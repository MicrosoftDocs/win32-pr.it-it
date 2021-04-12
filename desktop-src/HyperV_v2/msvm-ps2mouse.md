---
description: Rappresenta un dispositivo mouse PS2.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345776"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="3f78e-103">\_Classe MSVM Ps2mouse</span><span class="sxs-lookup"><span data-stu-id="3f78e-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="3f78e-104">Rappresenta un dispositivo mouse PS2.</span><span class="sxs-lookup"><span data-stu-id="3f78e-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="3f78e-105">Le istanze di questa classe sono periferiche logiche che sono sempre presenti in una macchina virtuale e pertanto non vengono allocate tramite un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f78e-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="3f78e-106">Un'istanza è sempre presente in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3f78e-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="3f78e-107">Questa classe non è disponibile per le macchine virtuali di seconda generazione.</span><span class="sxs-lookup"><span data-stu-id="3f78e-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="3f78e-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3f78e-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f78e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f78e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_PS2Mouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="3f78e-110">Members</span><span class="sxs-lookup"><span data-stu-id="3f78e-110">Members</span></span>

<span data-ttu-id="3f78e-111">La **classe \_ Ps2Mouse di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3f78e-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="3f78e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3f78e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3f78e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f78e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3f78e-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="3f78e-114">Methods</span></span>

<span data-ttu-id="3f78e-115">La **classe \_ Ps2Mouse di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3f78e-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="3f78e-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="3f78e-116">Method</span></span>                                                           | <span data-ttu-id="3f78e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f78e-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f78e-118">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="3f78e-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="3f78e-119">Simula un clic del pulsante, una sequenza di inattività, sul pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="3f78e-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="3f78e-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="3f78e-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="3f78e-122">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="3f78e-123">Recupera lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="3f78e-124">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="3f78e-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="3f78e-125">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="3f78e-126">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="3f78e-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="3f78e-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="3f78e-128">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3f78e-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="3f78e-129">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="3f78e-130">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3f78e-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="3f78e-131">Reimposta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f78e-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="3f78e-132">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="3f78e-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="3f78e-133">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="3f78e-134">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="3f78e-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="3f78e-135">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="3f78e-136">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="3f78e-137">Imposta lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="3f78e-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="3f78e-139">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="3f78e-140">**SetRelativePosition**</span><span class="sxs-lookup"><span data-stu-id="3f78e-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="3f78e-141">Compensa la posizione del puntatore del mouse in base ai Delta orizzontali e verticali specificati.</span><span class="sxs-lookup"><span data-stu-id="3f78e-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="3f78e-142">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="3f78e-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="3f78e-143">Regola la coordinata z del controllo rotellina del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="3f78e-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f78e-144">Properties</span></span>

<span data-ttu-id="3f78e-145">La **classe \_ Ps2Mouse di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3f78e-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f78e-146">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="3f78e-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3f78e-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-149">Indica se il dispositivo opera su coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="3f78e-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="3f78e-150">Se non è impostato, le coordinate del dispositivo sono relative.</span><span class="sxs-lookup"><span data-stu-id="3f78e-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="3f78e-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-152">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-154">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="3f78e-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="3f78e-155">La proprietà **Availability** indica lo stato primario e la disponibilità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f78e-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="3f78e-156">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3f78e-157">Valore</span><span class="sxs-lookup"><span data-stu-id="3f78e-157">Value</span></span>                                                                        | <span data-ttu-id="3f78e-158">Significato</span><span class="sxs-lookup"><span data-stu-id="3f78e-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3f78e-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="3f78e-160">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="3f78e-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3f78e-161">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="3f78e-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-162">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-164">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f78e-164">The primary availability and status of the device.</span></span> <span data-ttu-id="3f78e-165">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3f78e-166">Valore</span><span class="sxs-lookup"><span data-stu-id="3f78e-166">Value</span></span>                                                                        | <span data-ttu-id="3f78e-167">Significato</span><span class="sxs-lookup"><span data-stu-id="3f78e-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3f78e-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="3f78e-169">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="3f78e-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3f78e-170">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3f78e-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-171">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-173">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3f78e-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3f78e-174">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3f78e-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-175">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3f78e-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-178">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f78e-178">A short description of the object.</span></span> <span data-ttu-id="3f78e-179">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-180">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3f78e-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-181">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-183">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="3f78e-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3f78e-184">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3f78e-185">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3f78e-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3f78e-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="3f78e-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="3f78e-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="3f78e-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="3f78e-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3f78e-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3f78e-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3f78e-193">)</span><span class="sxs-lookup"><span data-stu-id="3f78e-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3f78e-194">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3f78e-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-197">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f78e-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-198">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="3f78e-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3f78e-199">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="3f78e-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="3f78e-200">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-201">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3f78e-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-204">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="3f78e-204">A description of the object.</span></span> <span data-ttu-id="3f78e-205">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3f78e-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-209">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3f78e-210">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3f78e-211">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3f78e-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="3f78e-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="3f78e-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="3f78e-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="3f78e-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="3f78e-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="3f78e-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3f78e-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3f78e-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3f78e-220">)</span><span class="sxs-lookup"><span data-stu-id="3f78e-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3f78e-221">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3f78e-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-224">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="3f78e-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-225">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3f78e-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="3f78e-226">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="3f78e-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3f78e-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-230">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f78e-230">A display name for the object.</span></span> <span data-ttu-id="3f78e-231">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="3f78e-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="3f78e-232">Anche la proprietà [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) della classe **CIM \_ ManagedSystemElement** è definita come nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="3f78e-233">Tuttavia, è spesso sottoclassato come una chiave.</span><span class="sxs-lookup"><span data-stu-id="3f78e-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="3f78e-234">Non è ragionevole che la stessa proprietà possa fornire identità e un nome visualizzato, senza incoerenze.</span><span class="sxs-lookup"><span data-stu-id="3f78e-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="3f78e-235">Dove [**Name**](msvm-keyboard.md) esiste e non è una chiave (ad esempio per le istanze di [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), le stesse informazioni possono essere presenti nelle proprietà **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3f78e-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="3f78e-236">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "mouse".</span><span class="sxs-lookup"><span data-stu-id="3f78e-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3f78e-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-240">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="3f78e-241">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f78e-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-243">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-245">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3f78e-246">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f78e-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-247">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3f78e-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-248">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3f78e-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-250">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="3f78e-251">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3f78e-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-255">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="3f78e-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="3f78e-256">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-257">**Mano**</span><span class="sxs-lookup"><span data-stu-id="3f78e-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-258">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-260">Configurazione del dispositivo di puntamento per l'operazione a destra o a sinistra.</span><span class="sxs-lookup"><span data-stu-id="3f78e-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="3f78e-261">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="3f78e-262">Valore</span><span class="sxs-lookup"><span data-stu-id="3f78e-262">Value</span></span>                                                                        | <span data-ttu-id="3f78e-263">Significato</span><span class="sxs-lookup"><span data-stu-id="3f78e-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="3f78e-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="3f78e-265">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="3f78e-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="3f78e-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3f78e-267">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="3f78e-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="3f78e-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3f78e-269">Operazione gestita a destra.</span><span class="sxs-lookup"><span data-stu-id="3f78e-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="3f78e-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3f78e-271">Operazione lasciata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="3f78e-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-273">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-275">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-275">The current health of the element.</span></span> <span data-ttu-id="3f78e-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK)</span><span class="sxs-lookup"><span data-stu-id="3f78e-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3f78e-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-278">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3f78e-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-280">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="3f78e-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="3f78e-281">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3f78e-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-283">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3f78e-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-285">Data e ora di creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3f78e-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="3f78e-286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3f78e-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-290">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="3f78e-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-291">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="3f78e-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3f78e-292">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="3f78e-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-294">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3f78e-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-296">Indica se il dispositivo è bloccato, impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3f78e-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="3f78e-297">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-298">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3f78e-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-299">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f78e-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-301">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3f78e-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="3f78e-302">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-303">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="3f78e-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-304">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f78e-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-306">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-306">This property has been deprecated.</span></span> <span data-ttu-id="3f78e-307">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-308">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3f78e-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-311">Qualificatori: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="3f78e-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-312">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="3f78e-312">The label by which the object is known.</span></span> <span data-ttu-id="3f78e-313">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="3f78e-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="3f78e-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-315">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="3f78e-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-316">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3f78e-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-318">Numero di pulsanti sul dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="3f78e-319">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3f78e-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-321">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-323">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3f78e-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3f78e-324">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3f78e-325">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3f78e-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3f78e-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="3f78e-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="3f78e-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="3f78e-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="3f78e-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="3f78e-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="3f78e-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="3f78e-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="3f78e-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="3f78e-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="3f78e-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="3f78e-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="3f78e-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="3f78e-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="3f78e-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="3f78e-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="3f78e-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3f78e-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3f78e-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3f78e-345">)</span><span class="sxs-lookup"><span data-stu-id="3f78e-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3f78e-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3f78e-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-347">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-349">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-349">The current status of the element.</span></span> <span data-ttu-id="3f78e-350">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="3f78e-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-351">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-354">Stato abilitato o disabilitato dell'elemento quando la proprietà [**EnabledState**](msvm-keyboard.md) è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="3f78e-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="3f78e-355">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="3f78e-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3f78e-356">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f78e-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3f78e-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-358">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3f78e-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-360">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3f78e-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="3f78e-361">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-362">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="3f78e-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-363">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-365">Tipo del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-365">The type of the pointing device.</span></span> <span data-ttu-id="3f78e-366">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="3f78e-367">Valore</span><span class="sxs-lookup"><span data-stu-id="3f78e-367">Value</span></span>                                                                        | <span data-ttu-id="3f78e-368">Significato</span><span class="sxs-lookup"><span data-stu-id="3f78e-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="3f78e-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3f78e-370">Mouse</span><span class="sxs-lookup"><span data-stu-id="3f78e-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3f78e-371">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3f78e-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-372">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-374">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f78e-374">The power management capabilities of the device.</span></span> <span data-ttu-id="3f78e-375">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-376">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3f78e-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-377">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3f78e-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-379">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="3f78e-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="3f78e-380">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-381">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3f78e-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-382">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f78e-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-384">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="3f78e-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="3f78e-385">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-386">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3f78e-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-389">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="3f78e-389">Provides high level status information.</span></span> <span data-ttu-id="3f78e-390">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="3f78e-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3f78e-391">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3f78e-392">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3f78e-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3f78e-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3f78e-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="3f78e-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="3f78e-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="3f78e-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3f78e-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3f78e-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3f78e-399">)</span><span class="sxs-lookup"><span data-stu-id="3f78e-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3f78e-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-401">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-403">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="3f78e-404">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f78e-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3f78e-405">Valore</span><span class="sxs-lookup"><span data-stu-id="3f78e-405">Value</span></span>                                                                         | <span data-ttu-id="3f78e-406">Significato</span><span class="sxs-lookup"><span data-stu-id="3f78e-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="3f78e-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3f78e-408">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="3f78e-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3f78e-409">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="3f78e-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-410">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f78e-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-412">Risoluzione del rilevamento del dispositivo di puntamento, in conteggi per pollice.</span><span class="sxs-lookup"><span data-stu-id="3f78e-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="3f78e-413">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-414">**Status**</span><span class="sxs-lookup"><span data-stu-id="3f78e-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-415">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-417">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3f78e-417">The current status of the object.</span></span> <span data-ttu-id="3f78e-418">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3f78e-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-420">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3f78e-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-422">Stringhe che descrivono i vari valori della matrice [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="3f78e-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="3f78e-423">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="3f78e-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3f78e-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-425">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-427">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3f78e-427">The current state of the logical device.</span></span> <span data-ttu-id="3f78e-428">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-429">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3f78e-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-432">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f78e-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-433">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="3f78e-433">The scoping system's creation class name.</span></span> <span data-ttu-id="3f78e-434">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-435">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3f78e-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3f78e-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-438">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3f78e-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-439">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="3f78e-439">The scoping system's name.</span></span> <span data-ttu-id="3f78e-440">Questo valore corrisponde al valore della proprietà [**Name**](msvm-computersystem.md) della classe **MSVM \_ ComputerSystem** per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="3f78e-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="3f78e-441">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3f78e-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-442">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3f78e-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-443">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3f78e-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-445">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3f78e-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3f78e-446">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="3f78e-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="3f78e-447">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="3f78e-448">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f78e-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-449">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3f78e-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-450">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f78e-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-452">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="3f78e-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="3f78e-453">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3f78e-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f78e-454">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3f78e-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f78e-455">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f78e-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f78e-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3f78e-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f78e-457">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3f78e-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3f78e-458">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3f78e-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f78e-459">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f78e-459">Remarks</span></span>

<span data-ttu-id="3f78e-460">L'accesso alla **classe \_ Ps2Mouse di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="3f78e-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3f78e-461">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3f78e-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f78e-462">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f78e-462">Requirements</span></span>



| <span data-ttu-id="3f78e-463">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f78e-463">Requirement</span></span> | <span data-ttu-id="3f78e-464">Valore</span><span class="sxs-lookup"><span data-stu-id="3f78e-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f78e-465">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f78e-465">Minimum supported client</span></span><br/> | <span data-ttu-id="3f78e-466">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3f78e-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f78e-467">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f78e-467">Minimum supported server</span></span><br/> | <span data-ttu-id="3f78e-468">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3f78e-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f78e-469">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3f78e-469">Namespace</span></span><br/>                | <span data-ttu-id="3f78e-470">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3f78e-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f78e-471">MOF</span><span class="sxs-lookup"><span data-stu-id="3f78e-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f78e-472"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f78e-473">DLL</span><span class="sxs-lookup"><span data-stu-id="3f78e-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f78e-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f78e-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f78e-475">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f78e-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f78e-476">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3f78e-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="3f78e-477">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3f78e-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="3f78e-478">Classi di input</span><span class="sxs-lookup"><span data-stu-id="3f78e-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

