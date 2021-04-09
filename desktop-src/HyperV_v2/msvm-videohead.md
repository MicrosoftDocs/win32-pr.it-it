---
description: Descrive la superficie di disegno principale in un controller di visualizzazione.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Classe Msvm_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130319"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="f3eac-103">\_Classe MSVM VideoHead</span><span class="sxs-lookup"><span data-stu-id="f3eac-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="f3eac-104">Descrive la superficie di disegno principale in un controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3eac-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="f3eac-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f3eac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3eac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3eac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
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
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="f3eac-107">Members</span><span class="sxs-lookup"><span data-stu-id="f3eac-107">Members</span></span>

<span data-ttu-id="f3eac-108">La **classe \_ VideoHead di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3eac-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="f3eac-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3eac-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f3eac-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3eac-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f3eac-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3eac-111">Methods</span></span>

<span data-ttu-id="f3eac-112">La **classe \_ VideoHead di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f3eac-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="f3eac-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="f3eac-113">Method</span></span>                                                          | <span data-ttu-id="f3eac-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3eac-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="f3eac-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f3eac-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="f3eac-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f3eac-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="f3eac-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="f3eac-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f3eac-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="f3eac-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="f3eac-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="f3eac-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3eac-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="f3eac-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="f3eac-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f3eac-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="f3eac-124">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3eac-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="f3eac-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="f3eac-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="f3eac-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f3eac-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f3eac-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="f3eac-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f3eac-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f3eac-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="f3eac-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f3eac-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3eac-131">Properties</span></span>

<span data-ttu-id="f3eac-132">La **classe \_ VideoHead di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3eac-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="f3eac-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-136">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eac-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="f3eac-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="f3eac-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="f3eac-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-141">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eac-141">The primary availability and status of the device.</span></span> <span data-ttu-id="f3eac-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3eac-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f3eac-143">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-143">Value</span></span>                                                                        | <span data-ttu-id="f3eac-144">Significato</span><span class="sxs-lookup"><span data-stu-id="f3eac-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f3eac-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f3eac-146">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f3eac-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3eac-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f3eac-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-148">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-150">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f3eac-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f3eac-151">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-152">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f3eac-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-155">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3eac-155">A short description of the object.</span></span> <span data-ttu-id="f3eac-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f3eac-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-160">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="f3eac-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f3eac-161">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3eac-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3eac-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f3eac-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="f3eac-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="f3eac-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="f3eac-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3eac-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3eac-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3eac-170">)</span><span class="sxs-lookup"><span data-stu-id="f3eac-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3eac-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3eac-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-174">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f3eac-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f3eac-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3eac-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-176">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="f3eac-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-179">Qualificatori: **unità** ("bits")</span><span class="sxs-lookup"><span data-stu-id="f3eac-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-180">Numero di bit utilizzati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="f3eac-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="f3eac-181">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-182">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="f3eac-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-185">Qualificatori: **unità** ("pixel")</span><span class="sxs-lookup"><span data-stu-id="f3eac-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-186">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="f3eac-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="f3eac-187">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-188">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="f3eac-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-189">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3eac-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-191">Il numero di colori supportati alle risoluzioni correnti.</span><span class="sxs-lookup"><span data-stu-id="f3eac-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="f3eac-192">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-193">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="f3eac-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-194">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-196">Se è in modalità carattere, il numero di colonne per il controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f3eac-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="f3eac-197">Altrimenti, è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="f3eac-197">Otherwise, 0.</span></span> <span data-ttu-id="f3eac-198">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-199">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="f3eac-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-200">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-202">Se è in modalità carattere, il numero di righe per questo controller video.</span><span class="sxs-lookup"><span data-stu-id="f3eac-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="f3eac-203">Altrimenti, è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="f3eac-203">Otherwise, 0.</span></span> <span data-ttu-id="f3eac-204">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-205">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f3eac-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-206">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-208">Qualificatori: **unità** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="f3eac-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-209">Frequenza di aggiornamento corrente, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="f3eac-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="f3eac-210">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-211">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="f3eac-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-214">Modalità di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="f3eac-214">The current scan mode.</span></span> <span data-ttu-id="f3eac-215">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3eac-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f3eac-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="f3eac-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operazione non interlacciata** (3)</span><span class="sxs-lookup"><span data-stu-id="f3eac-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operazione interlacciata** (4)</span><span class="sxs-lookup"><span data-stu-id="f3eac-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3eac-221">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="f3eac-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-222">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-224">Qualificatori: **unità** ("pixel")</span><span class="sxs-lookup"><span data-stu-id="f3eac-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-225">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="f3eac-225">The current number of vertical pixels.</span></span> <span data-ttu-id="f3eac-226">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-227">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f3eac-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-230">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f3eac-230">A description of the object.</span></span> <span data-ttu-id="f3eac-231">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f3eac-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-233">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-235">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f3eac-236">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3eac-237">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f3eac-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="f3eac-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="f3eac-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="f3eac-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="f3eac-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="f3eac-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3eac-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3eac-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3eac-246">)</span><span class="sxs-lookup"><span data-stu-id="f3eac-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3eac-247">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f3eac-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-250">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ Head \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="f3eac-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f3eac-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-254">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3eac-254">A display name for the object.</span></span> <span data-ttu-id="f3eac-255">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-256">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f3eac-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-259">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f3eac-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f3eac-260">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="f3eac-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="f3eac-261">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-261">Value</span></span>                                                                        | <span data-ttu-id="f3eac-262">Significato</span><span class="sxs-lookup"><span data-stu-id="f3eac-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f3eac-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f3eac-264">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f3eac-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="f3eac-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f3eac-266">Disabled</span><span class="sxs-lookup"><span data-stu-id="f3eac-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3eac-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f3eac-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-270">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f3eac-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f3eac-271">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="f3eac-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="f3eac-272">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f3eac-273">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-273">Value</span></span>                                                                        | <span data-ttu-id="f3eac-274">Significato</span><span class="sxs-lookup"><span data-stu-id="f3eac-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f3eac-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f3eac-276">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f3eac-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="f3eac-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="f3eac-278">Disabled</span><span class="sxs-lookup"><span data-stu-id="f3eac-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3eac-279">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f3eac-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-280">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3eac-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-282">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="f3eac-283">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f3eac-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-287">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="f3eac-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="f3eac-288">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f3eac-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-290">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-292">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3eac-292">The current health of the element.</span></span> <span data-ttu-id="f3eac-293">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f3eac-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f3eac-294">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="f3eac-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f3eac-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="f3eac-296">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-296">Value</span></span>                                                                        | <span data-ttu-id="f3eac-297">Significato</span><span class="sxs-lookup"><span data-stu-id="f3eac-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="f3eac-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="f3eac-299">OK</span><span class="sxs-lookup"><span data-stu-id="f3eac-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3eac-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f3eac-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-301">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f3eac-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-303">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="f3eac-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f3eac-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3eac-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-306">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3eac-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-308">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3eac-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f3eac-309">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f3eac-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-311">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-313">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f3eac-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-314">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f3eac-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f3eac-315">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f3eac-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-317">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-319">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3eac-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="f3eac-320">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-321">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="f3eac-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-322">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3eac-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-324">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-324">This property has been deprecated.</span></span> <span data-ttu-id="f3eac-325">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3eac-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-326">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f3eac-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-327">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-329">Qualificatori: **unità** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="f3eac-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-330">Frequenza di aggiornamento massima del controller di visualizzazione, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="f3eac-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="f3eac-331">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-332">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f3eac-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-333">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3eac-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-335">Qualificatori: **unità** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="f3eac-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-336">Frequenza di aggiornamento minima del controller video, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="f3eac-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="f3eac-337">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-338">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f3eac-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-341">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f3eac-341">The label by which the object is known.</span></span> <span data-ttu-id="f3eac-342">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="f3eac-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-343">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f3eac-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-346">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f3eac-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f3eac-347">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3eac-348">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3eac-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="f3eac-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="f3eac-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="f3eac-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="f3eac-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="f3eac-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="f3eac-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="f3eac-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="f3eac-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="f3eac-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="f3eac-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="f3eac-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="f3eac-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="f3eac-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="f3eac-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="f3eac-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="f3eac-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3eac-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3eac-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3eac-368">)</span><span class="sxs-lookup"><span data-stu-id="f3eac-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3eac-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f3eac-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-370">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-372">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3eac-372">The current statuses of the object.</span></span> <span data-ttu-id="f3eac-373">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-374">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="f3eac-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-375">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-377">Modalità di analisi corrente quando la proprietà **CurrentScanMode** dell'istanza è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f3eac-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="f3eac-378">Questa proprietà viene ereditata da [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)) ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-379">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f3eac-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-380">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-382">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f3eac-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f3eac-383">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="f3eac-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f3eac-384">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f3eac-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-386">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f3eac-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-388">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3eac-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f3eac-389">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-390">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f3eac-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-391">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-393">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3eac-393">The power management capabilities of the device.</span></span> <span data-ttu-id="f3eac-394">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f3eac-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-396">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f3eac-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-398">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="f3eac-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f3eac-399">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-400">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f3eac-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-401">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3eac-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-403">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="f3eac-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f3eac-404">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-405">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f3eac-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-406">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-408">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="f3eac-408">Provides high level status information.</span></span> <span data-ttu-id="f3eac-409">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f3eac-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f3eac-410">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f3eac-411">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f3eac-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f3eac-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f3eac-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="f3eac-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="f3eac-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f3eac-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f3eac-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f3eac-418">)</span><span class="sxs-lookup"><span data-stu-id="f3eac-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3eac-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f3eac-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-420">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-422">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3eac-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="f3eac-423">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="f3eac-424">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f3eac-425">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-425">Value</span></span>                                                                         | <span data-ttu-id="f3eac-426">Significato</span><span class="sxs-lookup"><span data-stu-id="f3eac-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f3eac-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f3eac-428">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f3eac-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3eac-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="f3eac-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-432">Stringa che specifica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f3eac-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="f3eac-433">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-434">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f3eac-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-435">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f3eac-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-437">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f3eac-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f3eac-438">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f3eac-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f3eac-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-440">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-442">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="f3eac-442">The current state of the logical device.</span></span> <span data-ttu-id="f3eac-443">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-444">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3eac-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-447">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3eac-447">The scoping system's creation class name.</span></span> <span data-ttu-id="f3eac-448">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3eac-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f3eac-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-450">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f3eac-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-452">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="f3eac-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="f3eac-453">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="f3eac-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-454">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f3eac-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-455">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3eac-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-456">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-457">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f3eac-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f3eac-458">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="f3eac-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-459">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f3eac-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-460">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3eac-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-462">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="f3eac-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f3eac-463">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="f3eac-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eac-464">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f3eac-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3eac-465">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f3eac-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f3eac-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3eac-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3eac-467">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f3eac-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f3eac-468">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f3eac-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f3eac-469">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-469">Value</span></span>                                                                         | <span data-ttu-id="f3eac-470">Significato</span><span class="sxs-lookup"><span data-stu-id="f3eac-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f3eac-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f3eac-472">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="f3eac-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3eac-473">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3eac-473">Remarks</span></span>

<span data-ttu-id="f3eac-474">L'accesso alla **classe \_ VideoHead di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f3eac-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f3eac-475">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f3eac-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eac-476">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3eac-476">Requirements</span></span>



| <span data-ttu-id="f3eac-477">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eac-477">Requirement</span></span> | <span data-ttu-id="f3eac-478">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eac-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eac-479">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3eac-479">Minimum supported client</span></span><br/> | <span data-ttu-id="f3eac-480">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f3eac-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f3eac-481">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3eac-481">Minimum supported server</span></span><br/> | <span data-ttu-id="f3eac-482">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f3eac-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3eac-483">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3eac-483">Namespace</span></span><br/>                | <span data-ttu-id="f3eac-484">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f3eac-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f3eac-485">MOF</span><span class="sxs-lookup"><span data-stu-id="f3eac-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3eac-486"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3eac-487">DLL</span><span class="sxs-lookup"><span data-stu-id="f3eac-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3eac-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3eac-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3eac-489">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3eac-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eac-490">**\_VIDEOHEAD CIM**</span><span class="sxs-lookup"><span data-stu-id="f3eac-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="f3eac-491">[**\_VIDEOHEAD CIM**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f3eac-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f3eac-492">Classi video</span><span class="sxs-lookup"><span data-stu-id="f3eac-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

