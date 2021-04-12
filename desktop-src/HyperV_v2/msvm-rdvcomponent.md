---
description: Rappresenta lo stato del componente RDV, che è responsabile della fornitura di un trasporto per l'elemento padre al Guest per scopi di configurazione.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231749"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="07b3c-103">\_Classe MSVM RdvComponent</span><span class="sxs-lookup"><span data-stu-id="07b3c-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="07b3c-104">Rappresenta lo stato del componente RDV, che è responsabile della fornitura di un trasporto per l'elemento padre al Guest per scopi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="07b3c-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="07b3c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="07b3c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b3c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07b3c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="07b3c-107">Members</span><span class="sxs-lookup"><span data-stu-id="07b3c-107">Members</span></span>

<span data-ttu-id="07b3c-108">La **classe \_ RdvComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07b3c-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="07b3c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="07b3c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="07b3c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07b3c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07b3c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="07b3c-111">Methods</span></span>

<span data-ttu-id="07b3c-112">La **classe \_ RdvComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="07b3c-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="07b3c-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="07b3c-113">Method</span></span>                                                       | <span data-ttu-id="07b3c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07b3c-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b3c-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="07b3c-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="07b3c-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="07b3c-117">**EnableEndPoints**</span><span class="sxs-lookup"><span data-stu-id="07b3c-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="07b3c-118">Richiede all'Servizi Desktop remoto dispositivo virtuale di avviare una connessione tramite pipe alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07b3c-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="07b3c-119">Se viene restituito zero (0), l'operazione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="07b3c-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="07b3c-120">Qualsiasi altro codice restituito indica una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="07b3c-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="07b3c-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="07b3c-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="07b3c-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="07b3c-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="07b3c-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="07b3c-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="07b3c-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="07b3c-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="07b3c-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="07b3c-127">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="07b3c-127">**Reset**</span></span>                                                    | <span data-ttu-id="07b3c-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="07b3c-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="07b3c-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="07b3c-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="07b3c-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="07b3c-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="07b3c-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="07b3c-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="07b3c-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="07b3c-134">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="07b3c-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07b3c-135">Properties</span></span>

<span data-ttu-id="07b3c-136">La **classe \_ RdvComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07b3c-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07b3c-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="07b3c-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-138">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-140">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07b3c-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="07b3c-141">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-142">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="07b3c-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-145">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07b3c-145">The primary availability and status of the device.</span></span> <span data-ttu-id="07b3c-146">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="07b3c-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="07b3c-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="07b3c-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="07b3c-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-152">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="07b3c-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-155">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="07b3c-155">A short description of the object.</span></span> <span data-ttu-id="07b3c-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="07b3c-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-160">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="07b3c-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="07b3c-161">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="07b3c-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="07b3c-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="07b3c-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3c-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3c-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3c-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3c-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="07b3c-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="07b3c-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="07b3c-170">)</span><span class="sxs-lookup"><span data-stu-id="07b3c-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07b3c-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="07b3c-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-174">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="07b3c-174">The scoping system's creation class name.</span></span> <span data-ttu-id="07b3c-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="07b3c-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-176">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="07b3c-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-179">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="07b3c-179">A description of the object.</span></span> <span data-ttu-id="07b3c-180">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="07b3c-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-184">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="07b3c-185">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="07b3c-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="07b3c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="07b3c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3c-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3c-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3c-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="07b3c-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3c-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="07b3c-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="07b3c-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="07b3c-195">)</span><span class="sxs-lookup"><span data-stu-id="07b3c-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07b3c-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="07b3c-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-199">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="07b3c-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="07b3c-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="07b3c-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="07b3c-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-204">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="07b3c-204">A display name for the object.</span></span> <span data-ttu-id="07b3c-205">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="07b3c-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-209">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="07b3c-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="07b3c-210">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="07b3c-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="07b3c-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-214">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="07b3c-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="07b3c-215">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="07b3c-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="07b3c-216">Valore</span><span class="sxs-lookup"><span data-stu-id="07b3c-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="07b3c-217">Significato</span><span class="sxs-lookup"><span data-stu-id="07b3c-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="07b3c-218"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="07b3c-219">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="07b3c-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="07b3c-220"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="07b3c-221"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="07b3c-222">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="07b3c-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="07b3c-223"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="07b3c-224">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="07b3c-225"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="07b3c-226">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="07b3c-227"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="07b3c-228">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="07b3c-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="07b3c-229"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="07b3c-230">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="07b3c-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="07b3c-231"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="07b3c-232">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="07b3c-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="07b3c-233"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="07b3c-234">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="07b3c-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="07b3c-235"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="07b3c-236">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="07b3c-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="07b3c-237">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="07b3c-238">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="07b3c-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="07b3c-239"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="07b3c-240">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="07b3c-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="07b3c-241">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="07b3c-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="07b3c-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="07b3c-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-243">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="07b3c-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-245">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="07b3c-246">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="07b3c-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-250">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="07b3c-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="07b3c-251">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="07b3c-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-253">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-255">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="07b3c-255">The current health of the element.</span></span> <span data-ttu-id="07b3c-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="07b3c-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-258">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="07b3c-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-260">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="07b3c-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="07b3c-261">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07b3c-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-263">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07b3c-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-265">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="07b3c-265">The date and time when the object was installed.</span></span> <span data-ttu-id="07b3c-266">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="07b3c-267">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="07b3c-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-271">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="07b3c-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-272">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="07b3c-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="07b3c-273">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="07b3c-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-275">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b3c-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-277">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="07b3c-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="07b3c-278">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="07b3c-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-280">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07b3c-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-282">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-282">This property has been deprecated.</span></span> <span data-ttu-id="07b3c-283">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-284">**Nome**</span><span class="sxs-lookup"><span data-stu-id="07b3c-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-287">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="07b3c-287">The label by which the object is known.</span></span> <span data-ttu-id="07b3c-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-289">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="07b3c-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-290">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-292">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="07b3c-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="07b3c-293">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="07b3c-294">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="07b3c-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="07b3c-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3c-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3c-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3c-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="07b3c-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="07b3c-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="07b3c-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="07b3c-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="07b3c-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="07b3c-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="07b3c-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="07b3c-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="07b3c-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="07b3c-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="07b3c-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="07b3c-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="07b3c-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="07b3c-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="07b3c-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="07b3c-314">)</span><span class="sxs-lookup"><span data-stu-id="07b3c-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07b3c-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="07b3c-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-316">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-318">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="07b3c-318">The current statuses of the object.</span></span> <span data-ttu-id="07b3c-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="07b3c-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-323">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="07b3c-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="07b3c-324">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="07b3c-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="07b3c-325">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="07b3c-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="07b3c-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-327">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="07b3c-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-329">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="07b3c-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="07b3c-330">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-331">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="07b3c-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-332">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-334">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07b3c-334">The power management capabilities of the device.</span></span> <span data-ttu-id="07b3c-335">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-336">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="07b3c-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-337">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="07b3c-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-339">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="07b3c-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="07b3c-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="07b3c-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-342">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07b3c-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-344">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="07b3c-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="07b3c-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-346">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="07b3c-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-347">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-349">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="07b3c-349">Provides high level status information.</span></span> <span data-ttu-id="07b3c-350">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="07b3c-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="07b3c-351">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="07b3c-352">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="07b3c-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="07b3c-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="07b3c-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="07b3c-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="07b3c-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="07b3c-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="07b3c-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="07b3c-359">)</span><span class="sxs-lookup"><span data-stu-id="07b3c-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="07b3c-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="07b3c-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-361">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-363">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="07b3c-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="07b3c-364">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="07b3c-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="07b3c-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-366">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-368">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="07b3c-368">The current status of the object.</span></span> <span data-ttu-id="07b3c-369">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-370">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="07b3c-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-371">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="07b3c-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-373">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="07b3c-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="07b3c-374">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="07b3c-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="07b3c-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-378">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="07b3c-378">The current state of the logical device.</span></span> <span data-ttu-id="07b3c-379">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-380">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="07b3c-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-383">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="07b3c-383">The scoping system's creation class name.</span></span> <span data-ttu-id="07b3c-384">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="07b3c-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-385">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="07b3c-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-386">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b3c-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-388">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="07b3c-388">The scoping system's name.</span></span> <span data-ttu-id="07b3c-389">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="07b3c-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-390">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="07b3c-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-391">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07b3c-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-393">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="07b3c-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="07b3c-394">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="07b3c-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-395">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="07b3c-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-396">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="07b3c-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-398">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="07b3c-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="07b3c-399">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="07b3c-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07b3c-400">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="07b3c-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b3c-401">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07b3c-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07b3c-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b3c-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b3c-403">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="07b3c-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="07b3c-404">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="07b3c-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07b3c-405">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07b3c-405">Requirements</span></span>



| <span data-ttu-id="07b3c-406">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b3c-406">Requirement</span></span> | <span data-ttu-id="07b3c-407">Valore</span><span class="sxs-lookup"><span data-stu-id="07b3c-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b3c-408">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07b3c-408">Minimum supported client</span></span><br/> | <span data-ttu-id="07b3c-409">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="07b3c-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="07b3c-410">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07b3c-410">Minimum supported server</span></span><br/> | <span data-ttu-id="07b3c-411">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="07b3c-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07b3c-412">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07b3c-412">Namespace</span></span><br/>                | <span data-ttu-id="07b3c-413">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="07b3c-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="07b3c-414">MOF</span><span class="sxs-lookup"><span data-stu-id="07b3c-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07b3c-415"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="07b3c-416">DLL</span><span class="sxs-lookup"><span data-stu-id="07b3c-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b3c-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07b3c-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

