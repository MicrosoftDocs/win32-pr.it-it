---
description: Rappresenta un dispositivo da tastiera.
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049996"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="3111b-103">\_Classe della tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="3111b-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="3111b-104">Rappresenta un dispositivo da tastiera.</span><span class="sxs-lookup"><span data-stu-id="3111b-104">Represents a keyboard device.</span></span> <span data-ttu-id="3111b-105">Le tastiere sono dispositivi logici che sono sempre presenti in una macchina virtuale e pertanto non vengono allocati tramite un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="3111b-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="3111b-106">Un'istanza è sempre presente in un sistema di computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="3111b-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="3111b-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3111b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3111b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3111b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Keyboard";
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
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="3111b-109">Members</span><span class="sxs-lookup"><span data-stu-id="3111b-109">Members</span></span>

<span data-ttu-id="3111b-110">La classe della **\_ tastiera MSVM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3111b-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="3111b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3111b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3111b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3111b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3111b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3111b-113">Methods</span></span>

<span data-ttu-id="3111b-114">La classe della **\_ tastiera MSVM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3111b-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="3111b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="3111b-115">Method</span></span>                                                         | <span data-ttu-id="3111b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3111b-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="3111b-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="3111b-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="3111b-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3111b-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="3111b-119">**Con pressione**</span><span class="sxs-lookup"><span data-stu-id="3111b-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="3111b-120">Recupera lo stato della chiave di una chiave.</span><span class="sxs-lookup"><span data-stu-id="3111b-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="3111b-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="3111b-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="3111b-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3111b-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="3111b-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="3111b-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="3111b-124">Simula la pressione di un tasto.</span><span class="sxs-lookup"><span data-stu-id="3111b-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="3111b-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="3111b-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="3111b-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3111b-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="3111b-127">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="3111b-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="3111b-128">Simula una versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="3111b-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="3111b-129">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3111b-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="3111b-130">Richiede che lo stato dell'elemento venga modificato.</span><span class="sxs-lookup"><span data-stu-id="3111b-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="3111b-131">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3111b-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="3111b-132">Reimposta la tastiera virtuale.</span><span class="sxs-lookup"><span data-stu-id="3111b-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="3111b-133">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="3111b-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="3111b-134">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3111b-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="3111b-135">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="3111b-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="3111b-136">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3111b-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="3111b-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3111b-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="3111b-138">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3111b-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="3111b-139">**TypeCtrlAltDel**</span><span class="sxs-lookup"><span data-stu-id="3111b-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="3111b-140">Simula una sequenza di tasti CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="3111b-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="3111b-141">**TypeKey**</span><span class="sxs-lookup"><span data-stu-id="3111b-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="3111b-142">Simula una sequenza di tasti stampa-rilascio.</span><span class="sxs-lookup"><span data-stu-id="3111b-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="3111b-143">**TypeScancodes**</span><span class="sxs-lookup"><span data-stu-id="3111b-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="3111b-144">Simula una sequenza di chiavi usando i codici di analisi.</span><span class="sxs-lookup"><span data-stu-id="3111b-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="3111b-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="3111b-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="3111b-146">Simula una serie di caratteri tipizzati.</span><span class="sxs-lookup"><span data-stu-id="3111b-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="3111b-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3111b-147">Properties</span></span>

<span data-ttu-id="3111b-148">La classe della **\_ tastiera MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3111b-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3111b-149">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="3111b-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-150">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-152">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="3111b-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="3111b-153">La proprietà **Availability** indica lo stato primario e la disponibilità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3111b-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="3111b-154">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3111b-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-155">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="3111b-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-156">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-158">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3111b-158">The primary availability and status of the device.</span></span> <span data-ttu-id="3111b-159">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3111b-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-160">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3111b-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-161">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-163">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3111b-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3111b-164">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3111b-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-165">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3111b-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3111b-168">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="3111b-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3111b-169">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3111b-169">A short description of the object.</span></span> <span data-ttu-id="3111b-170">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-171">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3111b-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-174">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="3111b-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3111b-175">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3111b-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3111b-176">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3111b-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3111b-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="3111b-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="3111b-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="3111b-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="3111b-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3111b-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3111b-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3111b-184">)</span><span class="sxs-lookup"><span data-stu-id="3111b-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3111b-185">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3111b-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3111b-188">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3111b-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3111b-189">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="3111b-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3111b-190">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="3111b-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="3111b-191">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3111b-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-192">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3111b-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-195">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="3111b-195">A description of the object.</span></span> <span data-ttu-id="3111b-196">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3111b-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-200">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="3111b-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3111b-201">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3111b-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3111b-202">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3111b-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="3111b-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="3111b-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="3111b-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="3111b-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="3111b-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="3111b-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3111b-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3111b-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3111b-211">)</span><span class="sxs-lookup"><span data-stu-id="3111b-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3111b-212">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3111b-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-215">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3111b-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="3111b-216">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="3111b-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="3111b-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3111b-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-220">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3111b-220">A display name for the object.</span></span> <span data-ttu-id="3111b-221">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="3111b-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="3111b-222">Anche la proprietà [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) della classe **CIM \_ ManagedSystemElement** è definita come nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3111b-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="3111b-223">Tuttavia, è spesso sottoclassato come una chiave.</span><span class="sxs-lookup"><span data-stu-id="3111b-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="3111b-224">Non è ragionevole che la stessa proprietà possa fornire identità e un nome visualizzato, senza incoerenze.</span><span class="sxs-lookup"><span data-stu-id="3111b-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="3111b-225">Dove **Name** esiste e non è una chiave (ad esempio per le istanze di [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), le stesse informazioni possono essere presenti nelle proprietà **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3111b-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="3111b-226">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3111b-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-228">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-230">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="3111b-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3111b-231">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3111b-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3111b-232">Valore</span><span class="sxs-lookup"><span data-stu-id="3111b-232">Value</span></span>                                                                        | <span data-ttu-id="3111b-233">Significato</span><span class="sxs-lookup"><span data-stu-id="3111b-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="3111b-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3111b-235">Abilitato</span><span class="sxs-lookup"><span data-stu-id="3111b-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3111b-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3111b-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-239">Indica gli stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="3111b-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="3111b-240">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="3111b-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3111b-241">Ad esempio, l'arresto (valore = 4) e l'avvio di (valore = 10) sono stati temporanei tra l'abilitazione e la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="3111b-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="3111b-242">Valore</span><span class="sxs-lookup"><span data-stu-id="3111b-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="3111b-243">Significato</span><span class="sxs-lookup"><span data-stu-id="3111b-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3111b-244"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="3111b-245">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="3111b-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="3111b-246"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="3111b-247">Altro</span><span class="sxs-lookup"><span data-stu-id="3111b-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="3111b-248"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="3111b-249">L'elemento è o potrebbe eseguire comandi, elaborerà tutti i comandi in coda e accoda le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="3111b-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="3111b-250"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="3111b-251">L'elemento non esegue i comandi e rilascia tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="3111b-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="3111b-252"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="3111b-253">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="3111b-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="3111b-254"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="3111b-255">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="3111b-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="3111b-256"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="3111b-257">È possibile che l'elemento stia completando i comandi e eliminerà tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="3111b-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="3111b-258"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="3111b-259">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="3111b-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="3111b-260"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="3111b-261">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="3111b-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="3111b-262"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="3111b-263">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="3111b-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="3111b-264">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="3111b-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="3111b-265">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="3111b-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="3111b-266"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="3111b-267">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="3111b-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="3111b-268">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="3111b-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3111b-269"><dt>**DMTF riservato**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="3111b-270">Questo valore è riservato.</span><span class="sxs-lookup"><span data-stu-id="3111b-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="3111b-271"><dt>**Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="3111b-272">Questo valore è riservato.</span><span class="sxs-lookup"><span data-stu-id="3111b-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="3111b-273">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3111b-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-274">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3111b-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-276">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="3111b-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="3111b-277">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3111b-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-281">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="3111b-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="3111b-282">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3111b-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-284">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-286">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3111b-286">The current health of the element.</span></span> <span data-ttu-id="3111b-287">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="3111b-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3111b-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-289">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3111b-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-291">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="3111b-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="3111b-292">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3111b-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3111b-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-294">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3111b-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-296">Data e ora di creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3111b-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="3111b-297">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3111b-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3111b-301">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="3111b-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3111b-302">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="3111b-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3111b-303">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="3111b-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-305">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3111b-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-307">Indica se il dispositivo è bloccato, impedendo l'input o l'output dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3111b-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="3111b-308">Questa proprietà viene ereditata da [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="3111b-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3111b-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-310">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3111b-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-312">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3111b-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="3111b-313">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-314">**Layout**</span><span class="sxs-lookup"><span data-stu-id="3111b-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-317">Stringa che indica il formato e il layout della tastiera.</span><span class="sxs-lookup"><span data-stu-id="3111b-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-318">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="3111b-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-319">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3111b-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-321">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="3111b-321">This property has been deprecated.</span></span> <span data-ttu-id="3111b-322">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-323">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3111b-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3111b-326">Qualificatori: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="3111b-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="3111b-327">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="3111b-327">The label by which the object is known.</span></span> <span data-ttu-id="3111b-328">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="3111b-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="3111b-329">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-330">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="3111b-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-331">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-333">Numero di tasti funzione sulla tastiera.</span><span class="sxs-lookup"><span data-stu-id="3111b-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-334">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3111b-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-335">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-337">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3111b-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3111b-338">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3111b-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3111b-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3111b-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3111b-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="3111b-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="3111b-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="3111b-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="3111b-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="3111b-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="3111b-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="3111b-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="3111b-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="3111b-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="3111b-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="3111b-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="3111b-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="3111b-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="3111b-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="3111b-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="3111b-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3111b-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3111b-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3111b-359">)</span><span class="sxs-lookup"><span data-stu-id="3111b-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3111b-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3111b-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-361">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-363">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3111b-363">The current status of the element.</span></span> <span data-ttu-id="3111b-364">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="3111b-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-365">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3111b-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-366">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-368">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="3111b-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3111b-369">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="3111b-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3111b-370">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3111b-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3111b-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-372">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3111b-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-374">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3111b-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="3111b-375">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3111b-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-376">**Password**</span><span class="sxs-lookup"><span data-stu-id="3111b-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-377">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-379">Indica se una password a livello di hardware è abilitata sulla tastiera, impedendo l'input locale.</span><span class="sxs-lookup"><span data-stu-id="3111b-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="3111b-380">5</span><span class="sxs-lookup"><span data-stu-id="3111b-380">5</span></span>
</dt> <dd>

<span data-ttu-id="3111b-381">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="3111b-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3111b-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3111b-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-383">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-385">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3111b-385">The power management capabilities of the device.</span></span> <span data-ttu-id="3111b-386">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3111b-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-388">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3111b-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-390">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="3111b-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="3111b-391">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3111b-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-393">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3111b-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-395">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="3111b-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="3111b-396">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3111b-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-398">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-400">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="3111b-400">Provides high level status information.</span></span> <span data-ttu-id="3111b-401">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="3111b-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3111b-402">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="3111b-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3111b-403">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3111b-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3111b-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3111b-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="3111b-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="3111b-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="3111b-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3111b-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3111b-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3111b-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3111b-410">)</span><span class="sxs-lookup"><span data-stu-id="3111b-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3111b-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3111b-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-412">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-414">Ultimo stato richiesto per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="3111b-414">The last requested state for the element.</span></span>



| <span data-ttu-id="3111b-415">Valore</span><span class="sxs-lookup"><span data-stu-id="3111b-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="3111b-416">Significato</span><span class="sxs-lookup"><span data-stu-id="3111b-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="3111b-417"><dt>**Non applicabile**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="3111b-418">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="3111b-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3111b-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="3111b-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-420">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-422">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3111b-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-424">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3111b-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3111b-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-426">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3111b-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3111b-427">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="3111b-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3111b-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3111b-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-429">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-431">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3111b-431">The current state of the logical device.</span></span> <span data-ttu-id="3111b-432">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3111b-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3111b-436">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3111b-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3111b-437">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="3111b-437">The scoping system's creation class name.</span></span> <span data-ttu-id="3111b-438">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="3111b-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="3111b-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3111b-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-440">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3111b-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3111b-442">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="3111b-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3111b-443">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="3111b-443">The scoping system's name.</span></span> <span data-ttu-id="3111b-444">Questo valore corrisponde al valore della proprietà **Name** della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="3111b-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="3111b-445">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3111b-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3111b-446">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3111b-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-447">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3111b-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-449">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3111b-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3111b-450">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="3111b-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="3111b-451">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="3111b-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="3111b-452">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3111b-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-453">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3111b-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-454">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3111b-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-456">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="3111b-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="3111b-457">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3111b-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-458">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3111b-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-459">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3111b-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-461">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3111b-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3111b-462">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="3111b-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3111b-463">**UnicodeSupported**</span><span class="sxs-lookup"><span data-stu-id="3111b-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3111b-464">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3111b-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3111b-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3111b-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3111b-466">Indica se la tastiera virtuale supporta i caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="3111b-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="3111b-467">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3111b-467">This can be one of the following values.</span></span>



| <span data-ttu-id="3111b-468">Valore</span><span class="sxs-lookup"><span data-stu-id="3111b-468">Value</span></span>                                                                            | <span data-ttu-id="3111b-469">Significato</span><span class="sxs-lookup"><span data-stu-id="3111b-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3111b-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="3111b-471">La tastiera virtuale supporta i caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="3111b-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="3111b-472"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="3111b-473">La tastiera virtuale non supporta i caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="3111b-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3111b-474">Commenti</span><span class="sxs-lookup"><span data-stu-id="3111b-474">Remarks</span></span>

<span data-ttu-id="3111b-475">L'accesso alla classe della **\_ tastiera MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="3111b-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3111b-476">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3111b-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3111b-477">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3111b-477">Requirements</span></span>



| <span data-ttu-id="3111b-478">Requisito</span><span class="sxs-lookup"><span data-stu-id="3111b-478">Requirement</span></span> | <span data-ttu-id="3111b-479">Valore</span><span class="sxs-lookup"><span data-stu-id="3111b-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3111b-480">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3111b-480">Minimum supported client</span></span><br/> | <span data-ttu-id="3111b-481">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3111b-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3111b-482">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3111b-482">Minimum supported server</span></span><br/> | <span data-ttu-id="3111b-483">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3111b-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3111b-484">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3111b-484">Namespace</span></span><br/>                | <span data-ttu-id="3111b-485">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3111b-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3111b-486">MOF</span><span class="sxs-lookup"><span data-stu-id="3111b-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3111b-487"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3111b-488">DLL</span><span class="sxs-lookup"><span data-stu-id="3111b-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3111b-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3111b-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3111b-490">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3111b-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3111b-491">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3111b-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="3111b-492">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3111b-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="3111b-493">Classi di input</span><span class="sxs-lookup"><span data-stu-id="3111b-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

