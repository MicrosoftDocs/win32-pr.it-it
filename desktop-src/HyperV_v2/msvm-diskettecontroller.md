---
description: Rappresenta il controller floppy nella macchina virtuale.
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Classe Msvm_DisketteController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751175"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="5eb3c-103">\_Classe MSVM DisketteController</span><span class="sxs-lookup"><span data-stu-id="5eb3c-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="5eb3c-104">Rappresenta il controller floppy nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="5eb3c-105">Il controller floppy è fisso, quindi non è associato alcun pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="5eb3c-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb3c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eb3c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName = "Msvm_DisketteController";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="5eb3c-108">Members</span><span class="sxs-lookup"><span data-stu-id="5eb3c-108">Members</span></span>

<span data-ttu-id="5eb3c-109">La **classe \_ DisketteController di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5eb3c-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="5eb3c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="5eb3c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5eb3c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb3c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5eb3c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5eb3c-112">Methods</span></span>

<span data-ttu-id="5eb3c-113">La **classe \_ DisketteController di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="5eb3c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="5eb3c-114">Method</span></span>                                                                   | <span data-ttu-id="5eb3c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eb3c-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="5eb3c-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="5eb3c-117">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5eb3c-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="5eb3c-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5eb3c-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="5eb3c-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="5eb3c-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="5eb3c-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="5eb3c-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="5eb3c-125">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="5eb3c-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="5eb3c-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5eb3c-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="5eb3c-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5eb3c-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="5eb3c-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5eb3c-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5eb3c-132">Properties</span></span>

<span data-ttu-id="5eb3c-133">La **classe \_ DisketteController di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5eb3c-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-135">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-141">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-142">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-143">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-145">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5eb3c-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5eb3c-146">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-147">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-150">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-150">A short description of the object.</span></span> <span data-ttu-id="5eb3c-151">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-152">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-155">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5eb3c-156">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5eb3c-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5eb3c-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5eb3c-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5eb3c-165">)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5eb3c-166">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-169">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5eb3c-170">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "MSVM \_ DisketteController".</span><span class="sxs-lookup"><span data-stu-id="5eb3c-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-171">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-174">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="5eb3c-174">A description of the object.</span></span> <span data-ttu-id="5eb3c-175">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-177">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-179">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5eb3c-180">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5eb3c-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5eb3c-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5eb3c-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5eb3c-190">)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5eb3c-191">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-194">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="5eb3c-195">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-199">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-199">A display name for the object.</span></span> <span data-ttu-id="5eb3c-200">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-201">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-204">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5eb3c-205">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-209">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5eb3c-210">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5eb3c-211">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5eb3c-212">Valore</span><span class="sxs-lookup"><span data-stu-id="5eb3c-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="5eb3c-213">Significato</span><span class="sxs-lookup"><span data-stu-id="5eb3c-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="5eb3c-214"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="5eb3c-215">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="5eb3c-216"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="5eb3c-217"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="5eb3c-218">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="5eb3c-219"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="5eb3c-220">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="5eb3c-221"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="5eb3c-222">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="5eb3c-223"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="5eb3c-224">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="5eb3c-225"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="5eb3c-226">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="5eb3c-227"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="5eb3c-228">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="5eb3c-229"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="5eb3c-230">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="5eb3c-231"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="5eb3c-232">L'elemento è abilitato, ma è in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="5eb3c-233">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="5eb3c-234">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="5eb3c-235"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="5eb3c-236">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="5eb3c-237">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="5eb3c-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-239">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-241">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-245">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-247">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-249">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-249">The current health of the element.</span></span> <span data-ttu-id="5eb3c-250">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5eb3c-251">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5eb3c-252">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-254">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-256">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-258">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-260">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5eb3c-261">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-265">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-266">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5eb3c-267">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-268">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-269">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-271">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-272">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-273">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-275">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="5eb3c-276">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="5eb3c-277">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="5eb3c-278">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)ed è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-280">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-282">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-283">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-286">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-286">The label by which the object is known.</span></span> <span data-ttu-id="5eb3c-287">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-288">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-289">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-291">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5eb3c-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5eb3c-292">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5eb3c-293">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5eb3c-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5eb3c-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5eb3c-313">)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5eb3c-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-315">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-317">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-317">The current statuses of the object.</span></span> <span data-ttu-id="5eb3c-318">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-319">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-322">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5eb3c-323">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5eb3c-324">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-326">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-329">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-330">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-332">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-333">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-334">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-336">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-337">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-338">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-341">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-342">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-344">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-344">Provides high level status information.</span></span> <span data-ttu-id="5eb3c-345">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5eb3c-346">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5eb3c-347">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5eb3c-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5eb3c-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5eb3c-354">)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5eb3c-355">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-358">Stringa che fornisce ulteriori informazioni correlate al protocollo supportato dal controller.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="5eb3c-359">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)ed è impostata su "Disk Protocol".</span><span class="sxs-lookup"><span data-stu-id="5eb3c-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-360">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-361">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-363">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="5eb3c-364">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)ed è impostata su 7 (dischetto flessibile).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-366">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-368">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="5eb3c-369">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5eb3c-370">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="5eb3c-371">Una particolare istanza di un elemento logico abilitato potrebbe non supportare **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="5eb3c-372">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="5eb3c-373">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-374">**Status**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-375">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-377">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-379">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-381">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5eb3c-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5eb3c-382">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-384">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-386">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-387">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-390">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-390">The scoping system's creation class name.</span></span> <span data-ttu-id="5eb3c-391">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-392">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-393">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-395">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="5eb3c-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-397">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-398">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-400">Ora dell'ultima accensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="5eb3c-401">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-402">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-403">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-405">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5eb3c-406">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-407">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-408">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-410">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5eb3c-411">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb3c-412">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5eb3c-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5eb3c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5eb3c-414">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5eb3c-415">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5eb3c-416">Commenti</span><span class="sxs-lookup"><span data-stu-id="5eb3c-416">Remarks</span></span>

<span data-ttu-id="5eb3c-417">L'accesso alla **classe \_ DisketteController di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5eb3c-418">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5eb3c-419">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eb3c-419">Requirements</span></span>



| <span data-ttu-id="5eb3c-420">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb3c-420">Requirement</span></span> | <span data-ttu-id="5eb3c-421">Valore</span><span class="sxs-lookup"><span data-stu-id="5eb3c-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb3c-422">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eb3c-422">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb3c-423">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5eb3c-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5eb3c-424">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eb3c-424">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb3c-425">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5eb3c-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5eb3c-426">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5eb3c-426">Namespace</span></span><br/>                | <span data-ttu-id="5eb3c-427">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5eb3c-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5eb3c-428">MOF</span><span class="sxs-lookup"><span data-stu-id="5eb3c-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eb3c-429"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5eb3c-430">DLL</span><span class="sxs-lookup"><span data-stu-id="5eb3c-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eb3c-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5eb3c-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5eb3c-432">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eb3c-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb3c-433">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="5eb3c-434">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="5eb3c-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="5eb3c-435">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5eb3c-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

