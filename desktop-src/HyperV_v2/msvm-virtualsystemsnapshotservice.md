---
description: Servizio per creare, applicare ed eliminare gli snapshot delle macchine virtuali.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878694"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="d2ee2-103">\_Classe MSVM VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="d2ee2-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="d2ee2-104">Servizio per creare, applicare ed eliminare gli snapshot delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="d2ee2-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ee2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2ee2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="d2ee2-107">Members</span><span class="sxs-lookup"><span data-stu-id="d2ee2-107">Members</span></span>

<span data-ttu-id="d2ee2-108">La **classe \_ VirtualSystemSnapshotService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d2ee2-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="d2ee2-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d2ee2-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2ee2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2ee2-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2ee2-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d2ee2-111">Methods</span></span>

<span data-ttu-id="d2ee2-112">La **classe \_ VirtualSystemSnapshotService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d2ee2-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="d2ee2-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d2ee2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2ee2-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d2ee2-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-116">Applica uno snapshot della macchina virtuale alla macchina virtuale dalla quale è stato creato.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d2ee2-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-118">Cancella lo stato di salvataggio da uno snapshot esistente.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d2ee2-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-120">Converte uno snapshot del sistema virtuale esistente in un punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="d2ee2-121">Lo snapshot viene eliminato come effetto collaterale.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="d2ee2-122">Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2ee2-123">Il supporto per questo metodo è stato aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d2ee2-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-125">Crea uno snapshot di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d2ee2-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-127">Elimina uno snapshot della macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="d2ee2-128">Questo metodo può, come effetto collaterale, eliminare altri snapshot che dipendono dallo snapshot interessato.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d2ee2-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-130">Rimuove uno snapshot esistente e tutti i relativi elementi figlio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d2ee2-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2ee2-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-132">Richiede una modifica di stato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2ee2-133">Il supporto per questo metodo è stato aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d2ee2-134"><strong>StartService</strong></span><span class="sxs-lookup"><span data-stu-id="d2ee2-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-135">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d2ee2-136"><strong>StopService</strong></span><span class="sxs-lookup"><span data-stu-id="d2ee2-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="d2ee2-137">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="d2ee2-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2ee2-138">Properties</span></span>

<span data-ttu-id="d2ee2-139">La **classe \_ VirtualSystemSnapshotService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2ee2-140">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-141">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-143">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="d2ee2-144">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d2ee2-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="d2ee2-145">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d2ee2-146">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d2ee2-147">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d2ee2-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="d2ee2-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d2ee2-158">)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ee2-159">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-162">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-162">A short description of the object.</span></span> <span data-ttu-id="d2ee2-163">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System snapshot Service".</span><span class="sxs-lookup"><span data-stu-id="d2ee2-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-167">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d2ee2-168">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ee2-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ee2-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ee2-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ee2-177">)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ee2-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-181">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-182">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d2ee2-183">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ VirtualSystemSnapshotService".</span><span class="sxs-lookup"><span data-stu-id="d2ee2-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-184">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-187">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="d2ee2-187">A description of the object.</span></span> <span data-ttu-id="d2ee2-188">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Service per la creazione, l'eliminazione definitiva e l'applicazione di snapshot di macchine virtuali".</span><span class="sxs-lookup"><span data-stu-id="d2ee2-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-192">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d2ee2-193">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ee2-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ee2-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ee2-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ee2-203">)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ee2-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-207">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-207">A display name for the object.</span></span> <span data-ttu-id="d2ee2-208">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-209">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-210">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-212">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d2ee2-213">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="d2ee2-214">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ee2-214">Value</span></span>                                                                        | <span data-ttu-id="d2ee2-215">Significato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="d2ee2-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d2ee2-217">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ee2-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-219">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-221">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d2ee2-222">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d2ee2-223">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="d2ee2-224">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ee2-224">Value</span></span>                                                                        | <span data-ttu-id="d2ee2-225">Significato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="d2ee2-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d2ee2-227">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ee2-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-229">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-231">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-231">The current health of the element.</span></span> <span data-ttu-id="d2ee2-232">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d2ee2-233">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d2ee2-234">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="d2ee2-235">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ee2-235">Value</span></span>                                                                        | <span data-ttu-id="d2ee2-236">Significato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d2ee2-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="d2ee2-238">Lo stato di integrità è Normal.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ee2-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-240">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-242">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d2ee2-243">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-247">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-248">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d2ee2-249">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-250">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-253">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-254">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-254">The label by which the object is known.</span></span> <span data-ttu-id="d2ee2-255">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "vssnapsvc".</span><span class="sxs-lookup"><span data-stu-id="d2ee2-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-259">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d2ee2-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d2ee2-260">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ee2-261">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ee2-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ee2-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ee2-281">)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ee2-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-283">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-285">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-285">The current statuses of the object.</span></span> <span data-ttu-id="d2ee2-286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-288">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-290">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d2ee2-291">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d2ee2-292">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-294">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-296">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-297">Tutte le informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="d2ee2-298">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-299">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-302">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-303">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="d2ee2-304">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="d2ee2-305">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-306">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-307">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-309">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-309">Provides high level status information.</span></span> <span data-ttu-id="d2ee2-310">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d2ee2-311">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ee2-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ee2-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ee2-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ee2-319">)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ee2-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-321">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-323">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="d2ee2-324">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d2ee2-325">Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="d2ee2-326">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="d2ee2-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="d2ee2-327">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d2ee2-328">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="d2ee2-329">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ee2-329">Value</span></span>                                                                         | <span data-ttu-id="d2ee2-330">Significato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="d2ee2-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d2ee2-332">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ee2-333">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-334">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-336">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="d2ee2-337">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-338">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-341">Qualificatori: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-342">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="d2ee2-343">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-344">**Status**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-347">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-348">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-349">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-351">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d2ee2-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d2ee2-352">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "il servizio è in esecuzione normalmente".</span><span class="sxs-lookup"><span data-stu-id="d2ee2-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-353">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-354">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-356">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-357">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-357">The scoping system's creation class name.</span></span> <span data-ttu-id="d2ee2-358">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="d2ee2-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-362">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d2ee2-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-363">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="d2ee2-364">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-366">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-368">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d2ee2-369">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ee2-370">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ee2-371">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ee2-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ee2-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2ee2-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ee2-373">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d2ee2-374">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ee2-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d2ee2-375">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ee2-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="d2ee2-376">Significato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d2ee2-377"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d2ee2-378"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d2ee2-379"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="d2ee2-380"><dt>**Arresta**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="d2ee2-381"><dt>**Nessuna modifica**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="d2ee2-382">Non è in corso alcuna transizione.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="d2ee2-383"><dt>**Offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="d2ee2-384"><dt>**Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="d2ee2-385"><dt>**Rinvia**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="d2ee2-386"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="d2ee2-387"><dt>**Riavvio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="d2ee2-388"><dt>**Reimposta**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="d2ee2-389"><dt>**Non applicabile**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="d2ee2-390">L'implementazione non supporta la rappresentazione delle transizioni in corso.</span><span class="sxs-lookup"><span data-stu-id="d2ee2-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="d2ee2-391"><dt> **DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2ee2-392">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2ee2-392">Requirements</span></span>



| <span data-ttu-id="d2ee2-393">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ee2-393">Requirement</span></span> | <span data-ttu-id="d2ee2-394">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ee2-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ee2-395">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-395">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ee2-396">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d2ee2-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2ee2-397">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2ee2-397">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ee2-398">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d2ee2-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2ee2-399">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2ee2-399">Namespace</span></span><br/>                | <span data-ttu-id="d2ee2-400">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2ee2-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2ee2-401">MOF</span><span class="sxs-lookup"><span data-stu-id="d2ee2-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2ee2-402"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2ee2-403">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ee2-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ee2-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2ee2-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

