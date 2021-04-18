---
description: Rappresenta un nodo NUMA (non-Uniform Memory Access) di un sistema virtuale.
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Classe Msvm_NumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318328"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="31187-103">\_Classe MSVM NumaNode</span><span class="sxs-lookup"><span data-stu-id="31187-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="31187-104">Rappresenta un nodo NUMA (non-Uniform Memory Access) di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="31187-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="31187-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="31187-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31187-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31187-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
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
  uint16   HealthState = 5;
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
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="31187-107">Members</span><span class="sxs-lookup"><span data-stu-id="31187-107">Members</span></span>

<span data-ttu-id="31187-108">La **classe \_ NumaNode di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="31187-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="31187-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="31187-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="31187-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31187-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31187-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="31187-111">Methods</span></span>

<span data-ttu-id="31187-112">La **classe \_ NumaNode di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="31187-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="31187-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="31187-113">Method</span></span>                 | <span data-ttu-id="31187-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31187-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="31187-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="31187-115">**RequestStateChange**</span></span> | <span data-ttu-id="31187-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="31187-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="31187-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31187-117">Properties</span></span>

<span data-ttu-id="31187-118">La **classe \_ NumaNode di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="31187-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31187-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="31187-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-120">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31187-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-122">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="31187-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="31187-123">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31187-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="31187-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="31187-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-127">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31187-127">A short description of the object.</span></span> <span data-ttu-id="31187-128">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="31187-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="31187-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-130">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-132">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="31187-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="31187-133">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="31187-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31187-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31187-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="31187-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31187-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="31187-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31187-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="31187-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31187-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="31187-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31187-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="31187-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31187-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="31187-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31187-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="31187-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31187-142">)</span><span class="sxs-lookup"><span data-stu-id="31187-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31187-143">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31187-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31187-146">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="31187-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="31187-147">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="31187-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="31187-148">**CurrentlyConsumableMemoryBlocks**</span><span class="sxs-lookup"><span data-stu-id="31187-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-149">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="31187-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="31187-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-151">Il numero di blocchi di memoria attualmente disponibili per l'utilizzo da parte delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="31187-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="31187-152">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="31187-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-155">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="31187-155">A description of the object.</span></span> <span data-ttu-id="31187-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="31187-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="31187-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-158">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-160">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="31187-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="31187-161">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="31187-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31187-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31187-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="31187-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31187-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="31187-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31187-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="31187-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31187-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="31187-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31187-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="31187-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31187-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="31187-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="31187-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="31187-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31187-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="31187-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31187-171">)</span><span class="sxs-lookup"><span data-stu-id="31187-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31187-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="31187-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-175">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31187-175">A display name for the object.</span></span> <span data-ttu-id="31187-176">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="31187-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-177">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="31187-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-180">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="31187-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="31187-181">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31187-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="31187-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="31187-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-185">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="31187-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="31187-186">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="31187-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="31187-187">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31187-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="31187-188">Valore</span><span class="sxs-lookup"><span data-stu-id="31187-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="31187-189">Significato</span><span class="sxs-lookup"><span data-stu-id="31187-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="31187-190"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31187-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="31187-191">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="31187-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="31187-192"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="31187-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="31187-193"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31187-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="31187-194">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31187-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="31187-195"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="31187-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="31187-196">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="31187-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="31187-197"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="31187-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="31187-198">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="31187-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="31187-199"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="31187-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="31187-200">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="31187-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="31187-201"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="31187-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="31187-202">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="31187-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="31187-203"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="31187-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="31187-204">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="31187-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="31187-205"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="31187-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="31187-206">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="31187-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="31187-207"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="31187-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="31187-208">L'elemento è abilitato, ma è in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="31187-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="31187-209">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="31187-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="31187-210">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="31187-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="31187-211"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="31187-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="31187-212">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="31187-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="31187-213">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="31187-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="31187-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="31187-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-215">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-217">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="31187-217">The current health of the element.</span></span> <span data-ttu-id="31187-218">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="31187-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="31187-219">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="31187-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="31187-220">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="31187-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="31187-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31187-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-222">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31187-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31187-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-224">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="31187-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="31187-225">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="31187-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31187-229">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="31187-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="31187-230">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="31187-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="31187-231">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="31187-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-232">**Nome**</span><span class="sxs-lookup"><span data-stu-id="31187-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-235">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="31187-235">The label by which the object is known.</span></span> <span data-ttu-id="31187-236">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-237">**NodeID**</span><span class="sxs-lookup"><span data-stu-id="31187-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-238">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31187-240">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31187-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="31187-241">Identificatore del nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="31187-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="31187-242">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="31187-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-243">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31187-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31187-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-245">Numero totale di core del processore logico in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="31187-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="31187-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="31187-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-247">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31187-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31187-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-249">Numero totale di core del processore in questo nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="31187-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="31187-250">Questo può essere diverso dal numero di [**oggetti \_ processore MSVM**](msvm-processor.md) associati a questo nodo se ogni core del processore supporta più thread di calcolo.</span><span class="sxs-lookup"><span data-stu-id="31187-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="31187-251">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="31187-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-252">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-254">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="31187-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="31187-255">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="31187-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31187-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31187-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="31187-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31187-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="31187-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31187-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="31187-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31187-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="31187-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31187-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="31187-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31187-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="31187-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="31187-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="31187-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="31187-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="31187-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="31187-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="31187-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="31187-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="31187-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="31187-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="31187-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="31187-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="31187-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="31187-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="31187-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="31187-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="31187-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="31187-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="31187-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="31187-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="31187-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="31187-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="31187-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="31187-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="31187-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31187-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="31187-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31187-276">)</span><span class="sxs-lookup"><span data-stu-id="31187-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31187-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="31187-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-278">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31187-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-280">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31187-280">The current statuses of the object.</span></span> <span data-ttu-id="31187-281">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-282">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="31187-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-283">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-285">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="31187-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="31187-286">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="31187-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="31187-287">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="31187-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="31187-288">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="31187-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-289">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-291">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="31187-291">Provides high level status information.</span></span> <span data-ttu-id="31187-292">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="31187-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="31187-293">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="31187-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31187-294">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31187-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="31187-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31187-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="31187-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31187-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="31187-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31187-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="31187-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31187-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="31187-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31187-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="31187-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31187-301">)</span><span class="sxs-lookup"><span data-stu-id="31187-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31187-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="31187-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-303">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-305">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="31187-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="31187-306">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="31187-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="31187-307">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="31187-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="31187-308">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="31187-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="31187-309">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="31187-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="31187-310">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="31187-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="31187-311">**Status**</span><span class="sxs-lookup"><span data-stu-id="31187-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="31187-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="31187-315">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="31187-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-316">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="31187-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="31187-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-318">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="31187-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="31187-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="31187-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="31187-320">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31187-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31187-323">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="31187-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="31187-324">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="31187-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="31187-325">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="31187-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31187-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31187-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31187-328">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="31187-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="31187-329">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="31187-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="31187-330">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="31187-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-331">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31187-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31187-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-333">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="31187-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="31187-334">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su "null".</span><span class="sxs-lookup"><span data-stu-id="31187-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="31187-335">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="31187-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31187-336">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31187-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31187-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31187-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31187-338">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="31187-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="31187-339">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31187-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31187-340">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31187-340">Requirements</span></span>



| <span data-ttu-id="31187-341">Requisito</span><span class="sxs-lookup"><span data-stu-id="31187-341">Requirement</span></span> | <span data-ttu-id="31187-342">Valore</span><span class="sxs-lookup"><span data-stu-id="31187-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31187-343">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31187-343">Minimum supported client</span></span><br/> | <span data-ttu-id="31187-344">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="31187-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31187-345">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31187-345">Minimum supported server</span></span><br/> | <span data-ttu-id="31187-346">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="31187-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31187-347">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31187-347">Namespace</span></span><br/>                | <span data-ttu-id="31187-348">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="31187-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="31187-349">MOF</span><span class="sxs-lookup"><span data-stu-id="31187-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31187-350"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31187-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31187-351">DLL</span><span class="sxs-lookup"><span data-stu-id="31187-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31187-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31187-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

