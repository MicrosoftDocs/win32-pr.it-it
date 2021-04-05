---
description: Indica lo stato di una sessione remota attiva che interagisce con una macchina virtuale.
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Classe Msvm_TerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759053"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="0b35c-103">\_Classe MSVM TerminalConnection</span><span class="sxs-lookup"><span data-stu-id="0b35c-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="0b35c-104">Indica lo stato di una sessione remota attiva che interagisce con una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b35c-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="0b35c-105">Può essere presente una sola connessione alla volta.</span><span class="sxs-lookup"><span data-stu-id="0b35c-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="0b35c-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0b35c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b35c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b35c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="0b35c-108">Members</span><span class="sxs-lookup"><span data-stu-id="0b35c-108">Members</span></span>

<span data-ttu-id="0b35c-109">La **classe \_ TerminalConnection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0b35c-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="0b35c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0b35c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b35c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b35c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b35c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0b35c-112">Methods</span></span>

<span data-ttu-id="0b35c-113">La **classe \_ TerminalConnection di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0b35c-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="0b35c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0b35c-114">Method</span></span>                                                                   | <span data-ttu-id="0b35c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b35c-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="0b35c-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0b35c-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="0b35c-117">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0b35c-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0b35c-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b35c-118">Properties</span></span>

<span data-ttu-id="0b35c-119">La **classe \_ TerminalConnection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b35c-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b35c-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0b35c-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-121">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-123">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="0b35c-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0b35c-124">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b35c-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0b35c-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-128">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b35c-128">A short description of the object.</span></span> <span data-ttu-id="0b35c-129">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0b35c-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-133">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="0b35c-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0b35c-134">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b35c-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b35c-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b35c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b35c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="0b35c-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="0b35c-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="0b35c-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="0b35c-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b35c-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b35c-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b35c-143">)</span><span class="sxs-lookup"><span data-stu-id="0b35c-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b35c-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="0b35c-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-147">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b35c-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-148">Identificatore univoco per un'istanza dell'oggetto connessione Terminal.</span><span class="sxs-lookup"><span data-stu-id="0b35c-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="0b35c-149">Il formato dell'identificatore è "Microsoft:*VMID* \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="0b35c-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="0b35c-150">Ad esempio, "Microsoft: 67A5D397-A02D-11DB-AC13-001676AA34F0 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="0b35c-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-151">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0b35c-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-154">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="0b35c-154">A description of the object.</span></span> <span data-ttu-id="0b35c-155">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0b35c-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-159">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="0b35c-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0b35c-160">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b35c-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b35c-161">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b35c-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="0b35c-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="0b35c-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="0b35c-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="0b35c-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="0b35c-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="0b35c-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b35c-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b35c-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b35c-170">)</span><span class="sxs-lookup"><span data-stu-id="0b35c-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b35c-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0b35c-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-174">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b35c-174">A display name for the object.</span></span> <span data-ttu-id="0b35c-175">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0b35c-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-177">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-179">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b35c-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0b35c-180">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b35c-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0b35c-181">Valore</span><span class="sxs-lookup"><span data-stu-id="0b35c-181">Value</span></span>                                                                        | <span data-ttu-id="0b35c-182">Significato</span><span class="sxs-lookup"><span data-stu-id="0b35c-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="0b35c-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0b35c-184">Abilitato</span><span class="sxs-lookup"><span data-stu-id="0b35c-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="0b35c-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0b35c-186">Disabled</span><span class="sxs-lookup"><span data-stu-id="0b35c-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b35c-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b35c-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-188">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-190">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b35c-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0b35c-191">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="0b35c-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0b35c-192">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b35c-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0b35c-193">Valore</span><span class="sxs-lookup"><span data-stu-id="0b35c-193">Value</span></span>                                                                        | <span data-ttu-id="0b35c-194">Significato</span><span class="sxs-lookup"><span data-stu-id="0b35c-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="0b35c-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0b35c-196">Abilitato</span><span class="sxs-lookup"><span data-stu-id="0b35c-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="0b35c-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0b35c-198">Disabled</span><span class="sxs-lookup"><span data-stu-id="0b35c-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="0b35c-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="0b35c-200">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0b35c-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b35c-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0b35c-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-204">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0b35c-204">The current health of the element.</span></span> <span data-ttu-id="0b35c-205">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="0b35c-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0b35c-206">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="0b35c-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0b35c-207">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="0b35c-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b35c-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-209">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b35c-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-211">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b35c-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0b35c-212">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b35c-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-216">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="0b35c-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-217">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0b35c-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0b35c-218">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-219">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0b35c-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-222">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="0b35c-222">The label by which the object is known.</span></span> <span data-ttu-id="0b35c-223">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="0b35c-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-224">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0b35c-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-225">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-227">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0b35c-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0b35c-228">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b35c-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b35c-229">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b35c-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b35c-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="0b35c-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="0b35c-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="0b35c-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="0b35c-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="0b35c-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="0b35c-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="0b35c-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="0b35c-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="0b35c-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="0b35c-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="0b35c-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="0b35c-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="0b35c-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="0b35c-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="0b35c-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="0b35c-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b35c-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b35c-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b35c-249">)</span><span class="sxs-lookup"><span data-stu-id="0b35c-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b35c-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0b35c-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-251">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-253">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b35c-253">The current statuses of the object.</span></span> <span data-ttu-id="0b35c-254">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-255">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b35c-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-258">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="0b35c-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0b35c-259">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="0b35c-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0b35c-260">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b35c-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-261">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0b35c-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-262">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-264">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="0b35c-264">Provides high level status information.</span></span> <span data-ttu-id="0b35c-265">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="0b35c-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0b35c-266">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="0b35c-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b35c-267">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0b35c-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0b35c-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0b35c-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="0b35c-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="0b35c-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b35c-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="0b35c-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0b35c-274">)</span><span class="sxs-lookup"><span data-stu-id="0b35c-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b35c-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0b35c-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-276">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-278">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0b35c-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="0b35c-279">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="0b35c-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0b35c-280">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0b35c-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0b35c-281">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="0b35c-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="0b35c-282">In tal caso, viene utilizzato il valore 12.</span><span class="sxs-lookup"><span data-stu-id="0b35c-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="0b35c-283">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.</span><span class="sxs-lookup"><span data-stu-id="0b35c-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="0b35c-284">Valore</span><span class="sxs-lookup"><span data-stu-id="0b35c-284">Value</span></span>                                                                         | <span data-ttu-id="0b35c-285">Significato</span><span class="sxs-lookup"><span data-stu-id="0b35c-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="0b35c-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0b35c-287">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0b35c-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b35c-288">**Status**</span><span class="sxs-lookup"><span data-stu-id="0b35c-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b35c-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-291">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b35c-291">The current status of the object.</span></span> <span data-ttu-id="0b35c-292">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="0b35c-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0b35c-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-294">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0b35c-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-296">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0b35c-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0b35c-297">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0b35c-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-298">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0b35c-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-299">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b35c-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-301">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0b35c-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0b35c-302">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="0b35c-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b35c-303">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0b35c-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b35c-304">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b35c-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b35c-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b35c-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b35c-306">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0b35c-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0b35c-307">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b35c-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0b35c-308">Valore</span><span class="sxs-lookup"><span data-stu-id="0b35c-308">Value</span></span>                                                                         | <span data-ttu-id="0b35c-309">Significato</span><span class="sxs-lookup"><span data-stu-id="0b35c-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="0b35c-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0b35c-311">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="0b35c-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b35c-312">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b35c-312">Remarks</span></span>

<span data-ttu-id="0b35c-313">L'accesso alla **classe \_ TerminalConnection di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="0b35c-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0b35c-314">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0b35c-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b35c-315">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b35c-315">Requirements</span></span>



| <span data-ttu-id="0b35c-316">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b35c-316">Requirement</span></span> | <span data-ttu-id="0b35c-317">Valore</span><span class="sxs-lookup"><span data-stu-id="0b35c-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b35c-318">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b35c-318">Minimum supported client</span></span><br/> | <span data-ttu-id="0b35c-319">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0b35c-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b35c-320">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b35c-320">Minimum supported server</span></span><br/> | <span data-ttu-id="0b35c-321">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0b35c-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b35c-322">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b35c-322">Namespace</span></span><br/>                | <span data-ttu-id="0b35c-323">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0b35c-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b35c-324">MOF</span><span class="sxs-lookup"><span data-stu-id="0b35c-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b35c-325"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b35c-326">DLL</span><span class="sxs-lookup"><span data-stu-id="0b35c-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b35c-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b35c-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b35c-328">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b35c-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b35c-329">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0b35c-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="0b35c-330">[**\_ENABLEDLOGICALELEMENT CIM**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b35c-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b35c-331">Classi video</span><span class="sxs-lookup"><span data-stu-id="0b35c-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

