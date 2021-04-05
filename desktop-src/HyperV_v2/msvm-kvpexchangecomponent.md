---
description: Rappresenta lo stato del servizio di scambio di coppie chiave/valore, che fornisce un meccanismo per lo scambio di dati tra la macchina virtuale e il sistema operativo in esecuzione nel sistema operativo di gestione.
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Classe Msvm_KvpExchangeComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885157"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="7770a-103">\_Classe MSVM KvpExchangeComponent</span><span class="sxs-lookup"><span data-stu-id="7770a-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="7770a-104">Rappresenta lo stato del servizio di scambio di coppie chiave/valore, che fornisce un meccanismo per lo scambio di dati tra la macchina virtuale e il sistema operativo in esecuzione nel sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="7770a-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="7770a-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7770a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7770a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7770a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="7770a-107">Members</span><span class="sxs-lookup"><span data-stu-id="7770a-107">Members</span></span>

<span data-ttu-id="7770a-108">La **classe \_ KvpExchangeComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7770a-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="7770a-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="7770a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7770a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7770a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7770a-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7770a-111">Methods</span></span>

<span data-ttu-id="7770a-112">La **classe \_ KvpExchangeComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7770a-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="7770a-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="7770a-113">Method</span></span>                                                                     | <span data-ttu-id="7770a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7770a-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="7770a-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="7770a-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="7770a-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7770a-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7770a-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="7770a-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="7770a-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7770a-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7770a-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="7770a-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="7770a-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7770a-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="7770a-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7770a-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="7770a-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="7770a-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="7770a-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7770a-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="7770a-124">Reimposta il componente.</span><span class="sxs-lookup"><span data-stu-id="7770a-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="7770a-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="7770a-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="7770a-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7770a-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7770a-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="7770a-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="7770a-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7770a-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7770a-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7770a-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="7770a-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7770a-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7770a-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7770a-131">Properties</span></span>

<span data-ttu-id="7770a-132">La **classe \_ KvpExchangeComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7770a-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7770a-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="7770a-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-136">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7770a-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="7770a-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="7770a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="7770a-138">Value</span></span>                                                                            | <span data-ttu-id="7770a-139">Significato</span><span class="sxs-lookup"><span data-stu-id="7770a-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7770a-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="7770a-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="7770a-142">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="7770a-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7770a-143">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="7770a-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-146">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7770a-146">The primary availability and status of the device.</span></span> <span data-ttu-id="7770a-147">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="7770a-148">Valore</span><span class="sxs-lookup"><span data-stu-id="7770a-148">Value</span></span>                                                                        | <span data-ttu-id="7770a-149">Significato</span><span class="sxs-lookup"><span data-stu-id="7770a-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7770a-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="7770a-151">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="7770a-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7770a-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="7770a-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-153">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-155">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="7770a-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="7770a-156">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-157">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7770a-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-160">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7770a-160">A short description of the object.</span></span> <span data-ttu-id="7770a-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7770a-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-165">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="7770a-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7770a-166">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7770a-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7770a-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7770a-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7770a-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="7770a-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="7770a-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="7770a-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="7770a-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7770a-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7770a-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7770a-175">)</span><span class="sxs-lookup"><span data-stu-id="7770a-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7770a-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7770a-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-179">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7770a-179">The scoping system's creation class name.</span></span> <span data-ttu-id="7770a-180">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-181">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7770a-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-184">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7770a-184">A description of the object.</span></span> <span data-ttu-id="7770a-185">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7770a-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-189">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="7770a-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7770a-190">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7770a-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7770a-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7770a-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="7770a-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="7770a-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="7770a-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="7770a-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="7770a-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="7770a-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7770a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7770a-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7770a-200">)</span><span class="sxs-lookup"><span data-stu-id="7770a-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7770a-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7770a-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-204">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7770a-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="7770a-205">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7770a-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-209">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7770a-209">A display name for the object.</span></span> <span data-ttu-id="7770a-210">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="7770a-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-214">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7770a-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7770a-215">Valore</span><span class="sxs-lookup"><span data-stu-id="7770a-215">Value</span></span>                                                                        | <span data-ttu-id="7770a-216">Significato</span><span class="sxs-lookup"><span data-stu-id="7770a-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="7770a-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="7770a-218">Nessun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="7770a-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7770a-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7770a-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-220">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-222">Stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7770a-222">The enabled state of the element.</span></span> <span data-ttu-id="7770a-223">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7770a-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7770a-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="7770a-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7770a-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7770a-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7770a-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-227">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7770a-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-229">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="7770a-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="7770a-230">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7770a-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-234">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="7770a-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="7770a-235">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-236">**GuestExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="7770a-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-237">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7770a-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7770a-239">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="7770a-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="7770a-240">Matrice di istanze di [**\_ KvpExchangeDataItem MSVM**](msvm-kvpexchangedataitem.md) incorporate che contengono il set di coppie chiave-valore che i servizi in esecuzione all'interno del sistema operativo guest hanno effettuato il push fino a essere disponibili per l'accesso da parte di client esterni.</span><span class="sxs-lookup"><span data-stu-id="7770a-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="7770a-241">Questa matrice non conterrà elementi intrinseci che vengono inseriti direttamente dal servizio di integrazione.</span><span class="sxs-lookup"><span data-stu-id="7770a-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="7770a-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-243">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7770a-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7770a-245">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="7770a-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="7770a-246">Matrice di istanze di [**\_ KvpExchangeDataItem MSVM**](msvm-kvpexchangedataitem.md) incorporate che contengono il set di coppie chiave-valore che il sistema operativo guest ha spinto a essere disponibile per l'accesso da parte di client esterni.</span><span class="sxs-lookup"><span data-stu-id="7770a-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="7770a-247">Questa matrice non conterrà gli elementi di dati inseriti da altri servizi in esecuzione nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="7770a-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7770a-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-249">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-251">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7770a-251">The current health of the element.</span></span> <span data-ttu-id="7770a-252">Questa operazione esprime l'integrità dell'elemento, ma non necessariamente quello dei sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7770a-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7770a-253">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="7770a-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7770a-254">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7770a-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-256">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7770a-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-258">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="7770a-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="7770a-259">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7770a-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-261">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7770a-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-263">Data e ora in cui il servizio di integrazione è stato installato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7770a-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="7770a-264">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7770a-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-266">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7770a-268">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7770a-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7770a-269">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7770a-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7770a-270">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7770a-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-272">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7770a-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-274">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7770a-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="7770a-275">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="7770a-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-277">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7770a-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-279">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="7770a-279">This property has been deprecated.</span></span> <span data-ttu-id="7770a-280">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-281">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7770a-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-284">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="7770a-284">The label by which the object is known.</span></span> <span data-ttu-id="7770a-285">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-286">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7770a-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-287">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-289">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7770a-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7770a-290">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7770a-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7770a-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7770a-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7770a-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="7770a-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="7770a-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="7770a-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="7770a-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="7770a-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="7770a-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="7770a-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="7770a-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="7770a-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="7770a-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="7770a-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="7770a-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="7770a-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="7770a-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="7770a-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="7770a-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7770a-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7770a-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7770a-311">)</span><span class="sxs-lookup"><span data-stu-id="7770a-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7770a-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7770a-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-313">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-315">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7770a-315">The current status of the element.</span></span> <span data-ttu-id="7770a-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="7770a-317">Di seguito sono riportati i valori possibili per il valore della proprietà **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="7770a-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="7770a-318">Valore</span><span class="sxs-lookup"><span data-stu-id="7770a-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="7770a-319">Significato</span><span class="sxs-lookup"><span data-stu-id="7770a-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="7770a-320"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="7770a-321">Il servizio funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="7770a-321">The service is operating normally.</span></span> <span data-ttu-id="7770a-322">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="7770a-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="7770a-323"><dt></dt> Ridotto <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="7770a-324">Il servizio funziona normalmente, ma il servizio Guest ha negoziato una versione del protocollo di comunicazione compatibile.</span><span class="sxs-lookup"><span data-stu-id="7770a-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="7770a-325">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="7770a-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="7770a-326"><dt>**Errore irreversibile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="7770a-327">Il Guest non supporta una versione del protocollo compatibile.</span><span class="sxs-lookup"><span data-stu-id="7770a-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="7770a-328">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="7770a-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="7770a-329"><dt>**Nessun contatto**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="7770a-330">Il servizio Guest non è installato o non è stato ancora contattato.</span><span class="sxs-lookup"><span data-stu-id="7770a-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="7770a-331"><dt>**Perdita di comunicazione**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="7770a-332">Il servizio Guest non risponde più normalmente.</span><span class="sxs-lookup"><span data-stu-id="7770a-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="7770a-333">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7770a-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-334">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-336">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7770a-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="7770a-337">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="7770a-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="7770a-338">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7770a-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7770a-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-340">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7770a-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-342">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7770a-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="7770a-343">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7770a-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7770a-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-345">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-347">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7770a-347">The power management capabilities of the device.</span></span> <span data-ttu-id="7770a-348">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7770a-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-350">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7770a-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-352">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="7770a-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="7770a-353">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="7770a-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-355">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7770a-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-357">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="7770a-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="7770a-358">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7770a-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-360">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-362">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="7770a-362">Provides high level status information.</span></span> <span data-ttu-id="7770a-363">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7770a-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7770a-364">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7770a-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7770a-365">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7770a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7770a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="7770a-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="7770a-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="7770a-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7770a-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7770a-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7770a-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7770a-372">)</span><span class="sxs-lookup"><span data-stu-id="7770a-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7770a-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7770a-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-374">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-376">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="7770a-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="7770a-377">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7770a-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7770a-378">Valore</span><span class="sxs-lookup"><span data-stu-id="7770a-378">Value</span></span>                                                                         | <span data-ttu-id="7770a-379">Significato</span><span class="sxs-lookup"><span data-stu-id="7770a-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7770a-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="7770a-381">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="7770a-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7770a-382">**Status**</span><span class="sxs-lookup"><span data-stu-id="7770a-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-383">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-385">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7770a-385">The current status of the object.</span></span> <span data-ttu-id="7770a-386">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-387">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7770a-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-388">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7770a-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7770a-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-390">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7770a-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7770a-391">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7770a-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7770a-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-393">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-395">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7770a-395">The current state of the logical device.</span></span> <span data-ttu-id="7770a-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-397">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7770a-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-398">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-400">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7770a-400">The scoping system's creation class name.</span></span> <span data-ttu-id="7770a-401">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7770a-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7770a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-405">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7770a-405">The scoping system's name.</span></span> <span data-ttu-id="7770a-406">Questo valore corrisponde al valore della proprietà [**Name**](msvm-computersystem.md) della classe **MSVM \_ ComputerSystem** per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="7770a-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="7770a-407">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7770a-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7770a-408">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7770a-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-409">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7770a-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-411">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7770a-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7770a-412">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-413">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="7770a-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-414">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7770a-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-416">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="7770a-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="7770a-417">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-418">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="7770a-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7770a-419">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7770a-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7770a-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7770a-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7770a-421">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7770a-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7770a-422">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7770a-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7770a-423">Commenti</span><span class="sxs-lookup"><span data-stu-id="7770a-423">Remarks</span></span>

<span data-ttu-id="7770a-424">L'accesso alla **classe \_ KvpExchangeComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="7770a-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7770a-425">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7770a-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7770a-426">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7770a-426">Requirements</span></span>



| <span data-ttu-id="7770a-427">Requisito</span><span class="sxs-lookup"><span data-stu-id="7770a-427">Requirement</span></span> | <span data-ttu-id="7770a-428">Valore</span><span class="sxs-lookup"><span data-stu-id="7770a-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7770a-429">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7770a-429">Minimum supported client</span></span><br/> | <span data-ttu-id="7770a-430">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7770a-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7770a-431">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7770a-431">Minimum supported server</span></span><br/> | <span data-ttu-id="7770a-432">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7770a-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7770a-433">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7770a-433">Namespace</span></span><br/>                | <span data-ttu-id="7770a-434">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7770a-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7770a-435">MOF</span><span class="sxs-lookup"><span data-stu-id="7770a-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7770a-436"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7770a-437">DLL</span><span class="sxs-lookup"><span data-stu-id="7770a-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7770a-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7770a-439">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7770a-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7770a-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7770a-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="7770a-441">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7770a-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

