---
description: Rappresenta un dispositivo mouse sintetico.
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750194"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="f3337-103">\_Classe MSVM SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="f3337-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="f3337-104">Rappresenta un dispositivo mouse sintetico.</span><span class="sxs-lookup"><span data-stu-id="f3337-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="f3337-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f3337-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3337-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3337-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
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
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="f3337-107">Members</span><span class="sxs-lookup"><span data-stu-id="f3337-107">Members</span></span>

<span data-ttu-id="f3337-108">La **classe \_ SyntheticMouse di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3337-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="f3337-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3337-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3337-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3337-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3337-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3337-111">Methods</span></span>

<span data-ttu-id="f3337-112">La **classe \_ SyntheticMouse di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f3337-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="f3337-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="f3337-113">Method</span></span>                                                                 | <span data-ttu-id="f3337-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3337-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="f3337-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="f3337-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="f3337-116">Simula un clic del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3337-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="f3337-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f3337-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="f3337-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3337-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="f3337-119">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="f3337-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="f3337-120">Recupera lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3337-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="f3337-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="f3337-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="f3337-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3337-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="f3337-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="f3337-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="f3337-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3337-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="f3337-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3337-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="f3337-126">Richiede una modifica dello stato</span><span class="sxs-lookup"><span data-stu-id="f3337-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="f3337-127">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f3337-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="f3337-128">Reimposta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3337-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="f3337-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="f3337-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="f3337-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3337-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="f3337-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f3337-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="f3337-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3337-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="f3337-133">**SetAbsolutePosition**</span><span class="sxs-lookup"><span data-stu-id="f3337-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="f3337-134">Imposta la posizione orizzontale e verticale del cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3337-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="f3337-135">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="f3337-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="f3337-136">Imposta lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3337-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="f3337-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f3337-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="f3337-138">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3337-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="f3337-139">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="f3337-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="f3337-140">Imposta la coordinata z del controllo rotellina del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f3337-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3337-141">Properties</span></span>

<span data-ttu-id="f3337-142">La **classe \_ SyntheticMouse di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3337-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3337-143">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="f3337-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3337-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-146">Indica se il dispositivo opera su coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="f3337-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="f3337-147">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-147">Value</span></span>                                                                                | <span data-ttu-id="f3337-148">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="f3337-149"><dt>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="f3337-150">Le coordinate del dispositivo sono assolute.</span><span class="sxs-lookup"><span data-stu-id="f3337-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="f3337-151"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="f3337-152">Le coordinate del dispositivo sono relative.</span><span class="sxs-lookup"><span data-stu-id="f3337-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3337-153">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="f3337-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-154">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-156">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="f3337-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="f3337-157">La proprietà **Availability** indica lo stato primario e la disponibilità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3337-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="f3337-158">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f3337-159">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-159">Value</span></span>                                                                          | <span data-ttu-id="f3337-160">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="f3337-161">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f3337-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3337-162">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f3337-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-165">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3337-165">The primary availability and status of the device.</span></span> <span data-ttu-id="f3337-166">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f3337-167">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-167">Value</span></span>                                                                        | <span data-ttu-id="f3337-168">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f3337-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f3337-170">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f3337-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3337-171">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f3337-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-172">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-174">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f3337-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f3337-175">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3337-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-176">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f3337-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-179">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3337-179">A short description of the object.</span></span> <span data-ttu-id="f3337-180">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-181">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f3337-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-184">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="f3337-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f3337-185">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3337-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3337-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3337-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3337-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f3337-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="f3337-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="f3337-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="f3337-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3337-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3337-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3337-194">)</span><span class="sxs-lookup"><span data-stu-id="f3337-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3337-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3337-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-198">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f3337-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3337-199">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f3337-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f3337-200">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f3337-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="f3337-201">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-202">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f3337-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-205">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f3337-205">A description of the object.</span></span> <span data-ttu-id="f3337-206">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f3337-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-210">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="f3337-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f3337-211">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3337-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3337-212">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3337-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f3337-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="f3337-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="f3337-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="f3337-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="f3337-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="f3337-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3337-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3337-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3337-221">)</span><span class="sxs-lookup"><span data-stu-id="f3337-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3337-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f3337-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-225">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="f3337-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3337-226">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3337-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="f3337-227">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="f3337-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="f3337-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f3337-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-231">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3337-231">A display name for the object.</span></span> <span data-ttu-id="f3337-232">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="f3337-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="f3337-233">Anche la proprietà [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) della classe **CIM \_ ManagedSystemElement** è definita come nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f3337-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="f3337-234">Tuttavia, è spesso sottoclassato come una chiave.</span><span class="sxs-lookup"><span data-stu-id="f3337-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="f3337-235">Non è ragionevole che la stessa proprietà possa fornire identità e un nome visualizzato, senza incoerenze.</span><span class="sxs-lookup"><span data-stu-id="f3337-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="f3337-236">Dove [**Name**](msvm-keyboard.md) esiste e non è una chiave, ad esempio per le istanze di LogicalDevice, le stesse informazioni possono essere presenti nelle proprietà **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="f3337-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="f3337-237">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f3337-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-239">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-241">Configurazione predefinita o di avvio di un amministratore per la **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f3337-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="f3337-242">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3337-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f3337-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-246">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f3337-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f3337-247">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3337-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f3337-248">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="f3337-249">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="f3337-250"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f3337-251">La macchina virtuale guest supporta un mouse sintetico.</span><span class="sxs-lookup"><span data-stu-id="f3337-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="f3337-252"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f3337-253">La macchina virtuale guest non supporta un mouse sintetico.</span><span class="sxs-lookup"><span data-stu-id="f3337-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3337-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f3337-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-255">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3337-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-257">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f3337-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="f3337-258">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f3337-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-262">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f3337-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="f3337-263">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-264">**Mano**</span><span class="sxs-lookup"><span data-stu-id="f3337-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-265">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-267">Configurazione del dispositivo di puntamento per l'operazione a destra o a sinistra.</span><span class="sxs-lookup"><span data-stu-id="f3337-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="f3337-268">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="f3337-269">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-269">Value</span></span>                                                                        | <span data-ttu-id="f3337-270">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="f3337-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="f3337-272">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f3337-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="f3337-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f3337-274">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="f3337-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="f3337-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f3337-276">Operazione gestita a destra.</span><span class="sxs-lookup"><span data-stu-id="f3337-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="f3337-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f3337-278">Operazione lasciata.</span><span class="sxs-lookup"><span data-stu-id="f3337-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="f3337-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f3337-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-280">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-282">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3337-282">The current health of the element.</span></span> <span data-ttu-id="f3337-283">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="f3337-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-285">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3337-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-287">Coordinata x assoluta del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f3337-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-289">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f3337-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-291">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="f3337-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="f3337-292">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3337-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-294">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3337-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-296">Data e ora di creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3337-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="f3337-297">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f3337-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-301">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f3337-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f3337-302">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f3337-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f3337-303">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="f3337-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-305">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3337-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-307">Indica se il dispositivo è bloccato, impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f3337-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="f3337-308">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f3337-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-310">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3337-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-312">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3337-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="f3337-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-314">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="f3337-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-315">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3337-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-317">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="f3337-317">This property has been deprecated.</span></span> <span data-ttu-id="f3337-318">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f3337-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-322">Qualificatori: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="f3337-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f3337-323">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f3337-323">The label by which the object is known.</span></span> <span data-ttu-id="f3337-324">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f3337-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="f3337-325">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-326">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="f3337-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-327">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3337-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-329">Numero di pulsanti sul dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="f3337-330">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-331">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f3337-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-332">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-334">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f3337-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f3337-335">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3337-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3337-336">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3337-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3337-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f3337-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="f3337-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="f3337-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="f3337-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="f3337-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="f3337-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="f3337-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="f3337-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="f3337-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="f3337-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="f3337-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="f3337-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="f3337-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="f3337-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="f3337-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="f3337-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3337-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3337-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3337-356">)</span><span class="sxs-lookup"><span data-stu-id="f3337-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3337-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f3337-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-358">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-360">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3337-360">The current status of the element.</span></span> <span data-ttu-id="f3337-361">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f3337-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-363">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-365">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f3337-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f3337-366">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="f3337-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f3337-367">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3337-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f3337-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-369">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f3337-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-371">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3337-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f3337-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-373">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="f3337-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-374">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-376">Tipo di dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-376">The type of pointing device.</span></span> <span data-ttu-id="f3337-377">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="f3337-378">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-378">Value</span></span>                                                                        | <span data-ttu-id="f3337-379">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="f3337-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f3337-381">Mouse</span><span class="sxs-lookup"><span data-stu-id="f3337-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3337-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f3337-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-383">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-385">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3337-385">The power management capabilities of the device.</span></span> <span data-ttu-id="f3337-386">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f3337-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-388">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3337-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-390">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="f3337-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f3337-391">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f3337-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-393">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3337-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-395">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="f3337-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f3337-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f3337-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-398">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-400">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="f3337-400">Provides high level status information.</span></span> <span data-ttu-id="f3337-401">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f3337-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f3337-402">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3337-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3337-403">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3337-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3337-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f3337-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="f3337-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="f3337-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3337-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3337-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3337-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3337-410">)</span><span class="sxs-lookup"><span data-stu-id="f3337-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3337-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f3337-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-412">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-414">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3337-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="f3337-415">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3337-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f3337-416">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-416">Value</span></span>                                                                         | <span data-ttu-id="f3337-417">Significato</span><span class="sxs-lookup"><span data-stu-id="f3337-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f3337-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f3337-419">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f3337-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3337-420">**Risoluzione**</span><span class="sxs-lookup"><span data-stu-id="f3337-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-421">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3337-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-423">Risoluzione del rilevamento del dispositivo di puntamento, in conteggi per pollice.</span><span class="sxs-lookup"><span data-stu-id="f3337-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="f3337-424">Questa proprietà viene ereditata da [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-425">**ScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="f3337-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-426">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3337-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-427">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-428">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickey")</span><span class="sxs-lookup"><span data-stu-id="f3337-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="f3337-429">Posizione della coordinata z del dispositivo mouse.</span><span class="sxs-lookup"><span data-stu-id="f3337-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="f3337-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-431">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-433">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3337-433">The current status of the object.</span></span> <span data-ttu-id="f3337-434">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-435">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f3337-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-436">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f3337-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3337-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-438">Stringhe che descrivono i vari valori della matrice [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="f3337-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="f3337-439">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3337-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f3337-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-441">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-443">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3337-443">The current state of the logical device.</span></span> <span data-ttu-id="f3337-444">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-445">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3337-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-446">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-448">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f3337-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3337-449">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3337-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="f3337-450">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f3337-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-452">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3337-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3337-454">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f3337-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3337-455">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3337-455">The name of the scoping system.</span></span> <span data-ttu-id="f3337-456">Questo valore corrisponde al valore della proprietà [**Name**](msvm-computersystem.md) della classe **MSVM \_ ComputerSystem** per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3337-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="f3337-457">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3337-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3337-458">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3337-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-459">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3337-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-461">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3337-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f3337-462">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="f3337-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="f3337-463">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="f3337-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="f3337-464">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3337-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f3337-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-466">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3337-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-467">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-468">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="f3337-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f3337-469">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3337-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-470">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f3337-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-471">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3337-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-473">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f3337-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f3337-474">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3337-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3337-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="f3337-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3337-476">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3337-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3337-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3337-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3337-478">Coordinata y assoluta del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="f3337-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3337-479">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3337-479">Remarks</span></span>

<span data-ttu-id="f3337-480">L'accesso alla **classe \_ SyntheticMouse di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f3337-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f3337-481">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f3337-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3337-482">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3337-482">Requirements</span></span>



| <span data-ttu-id="f3337-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3337-483">Requirement</span></span> | <span data-ttu-id="f3337-484">Valore</span><span class="sxs-lookup"><span data-stu-id="f3337-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3337-485">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3337-485">Minimum supported client</span></span><br/> | <span data-ttu-id="f3337-486">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f3337-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f3337-487">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3337-487">Minimum supported server</span></span><br/> | <span data-ttu-id="f3337-488">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f3337-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3337-489">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3337-489">Namespace</span></span><br/>                | <span data-ttu-id="f3337-490">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f3337-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f3337-491">MOF</span><span class="sxs-lookup"><span data-stu-id="f3337-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3337-492"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3337-493">DLL</span><span class="sxs-lookup"><span data-stu-id="f3337-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3337-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3337-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3337-495">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3337-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3337-496">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f3337-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="f3337-497">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f3337-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="f3337-498">Classi di input</span><span class="sxs-lookup"><span data-stu-id="f3337-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

