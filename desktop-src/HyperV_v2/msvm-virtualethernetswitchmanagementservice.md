---
description: Rappresenta il servizio di virtualizzazione presente in un singolo sistema host. MSVM \_ VirtualEthernetSwitchManagementService viene usato per controllare la definizione, la modifica e l'eliminazione dei commutatori Ethernet virtuali.
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320003"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="d62af-104">\_Classe MSVM VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="d62af-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="d62af-105">Rappresenta il servizio di virtualizzazione presente in un singolo sistema host.</span><span class="sxs-lookup"><span data-stu-id="d62af-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="d62af-106">MSVM \_ VirtualEthernetSwitchManagementService viene usato per controllare la definizione, la modifica e l'eliminazione dei commutatori Ethernet virtuali.</span><span class="sxs-lookup"><span data-stu-id="d62af-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="d62af-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d62af-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d62af-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d62af-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="d62af-109">Members</span><span class="sxs-lookup"><span data-stu-id="d62af-109">Members</span></span>

<span data-ttu-id="d62af-110">La **classe \_ VirtualEthernetSwitchManagementService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d62af-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="d62af-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d62af-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d62af-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d62af-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d62af-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="d62af-113">Methods</span></span>

<span data-ttu-id="d62af-114">La **classe \_ VirtualEthernetSwitchManagementService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d62af-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="d62af-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="d62af-115">Method</span></span>                                                                                               | <span data-ttu-id="d62af-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d62af-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="d62af-117">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="d62af-118">Aggiunge le impostazioni della funzionalità alla configurazione di una porta di commutazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d62af-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="d62af-119">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="d62af-120">Aggiunge risorse a una configurazione di Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="d62af-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="d62af-121">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="d62af-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="d62af-122">Crea un nuovo commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="d62af-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="d62af-123">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="d62af-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="d62af-124">Elimina definitivamente un commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="d62af-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="d62af-125">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="d62af-126">Modifica le impostazioni delle funzionalità di una porta di commutazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d62af-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="d62af-127">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="d62af-128">Modifica le impostazioni delle risorse per un commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="d62af-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="d62af-129">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="d62af-130">Modifica le impostazioni del Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="d62af-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="d62af-131">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="d62af-132">Rimuove le impostazioni della funzionalità da una porta di commutazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="d62af-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="d62af-133">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="d62af-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="d62af-134">Rimuove le impostazioni delle risorse virtuali da una configurazione di commutiri virtuali.</span><span class="sxs-lookup"><span data-stu-id="d62af-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="d62af-135">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d62af-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="d62af-136">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="d62af-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="d62af-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="d62af-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="d62af-138">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="d62af-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="d62af-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="d62af-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="d62af-140">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="d62af-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="d62af-141">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d62af-141">Properties</span></span>

<span data-ttu-id="d62af-142">La **classe \_ VirtualEthernetSwitchManagementService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d62af-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d62af-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d62af-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-144">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d62af-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-146">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d62af-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d62af-147">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d62af-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d62af-148">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d62af-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-151">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d62af-151">A short description of the object.</span></span> <span data-ttu-id="d62af-152">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V virtual networking Management Service".</span><span class="sxs-lookup"><span data-stu-id="d62af-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-153">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d62af-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-156">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="d62af-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d62af-157">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d62af-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d62af-158">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d62af-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d62af-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d62af-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="d62af-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="d62af-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="d62af-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="d62af-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d62af-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d62af-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d62af-166">)</span><span class="sxs-lookup"><span data-stu-id="d62af-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d62af-167">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d62af-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-170">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d62af-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-171">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="d62af-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d62af-172">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ VirtualEthernetSwitchManagementService".</span><span class="sxs-lookup"><span data-stu-id="d62af-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-173">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d62af-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-176">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="d62af-176">A description of the object.</span></span> <span data-ttu-id="d62af-177">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "fornisce la gestione WMI per la rete Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="d62af-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d62af-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-181">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="d62af-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d62af-182">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d62af-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d62af-183">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d62af-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d62af-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="d62af-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="d62af-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="d62af-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="d62af-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="d62af-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="d62af-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d62af-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d62af-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d62af-192">)</span><span class="sxs-lookup"><span data-stu-id="d62af-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d62af-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d62af-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-196">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d62af-196">A display name for the object.</span></span> <span data-ttu-id="d62af-197">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V networking Management Service".</span><span class="sxs-lookup"><span data-stu-id="d62af-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d62af-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-201">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d62af-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d62af-202">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="d62af-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="d62af-203">Valore</span><span class="sxs-lookup"><span data-stu-id="d62af-203">Value</span></span>                                                                        | <span data-ttu-id="d62af-204">Significato</span><span class="sxs-lookup"><span data-stu-id="d62af-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="d62af-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d62af-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d62af-206">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d62af-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d62af-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d62af-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-210">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d62af-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d62af-211">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="d62af-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d62af-212">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d62af-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d62af-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d62af-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-214">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-216">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d62af-216">The current health of the element.</span></span> <span data-ttu-id="d62af-217">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d62af-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d62af-218">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="d62af-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d62af-219">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="d62af-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="d62af-220">Valore</span><span class="sxs-lookup"><span data-stu-id="d62af-220">Value</span></span>                                                                        | <span data-ttu-id="d62af-221">Significato</span><span class="sxs-lookup"><span data-stu-id="d62af-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d62af-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d62af-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="d62af-223">Lo stato di integrità è Normal.</span><span class="sxs-lookup"><span data-stu-id="d62af-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d62af-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d62af-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-225">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d62af-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-227">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d62af-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d62af-228">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d62af-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d62af-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d62af-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-232">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d62af-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d62af-233">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d62af-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d62af-234">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d62af-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d62af-235">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d62af-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-238">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d62af-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-239">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="d62af-239">The label by which the object is known.</span></span> <span data-ttu-id="d62af-240">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "VMMS".</span><span class="sxs-lookup"><span data-stu-id="d62af-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-241">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d62af-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-242">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-244">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d62af-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d62af-245">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d62af-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d62af-246">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d62af-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d62af-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d62af-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="d62af-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="d62af-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="d62af-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="d62af-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="d62af-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="d62af-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="d62af-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="d62af-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="d62af-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="d62af-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="d62af-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="d62af-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="d62af-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="d62af-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="d62af-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="d62af-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d62af-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d62af-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d62af-266">)</span><span class="sxs-lookup"><span data-stu-id="d62af-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d62af-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d62af-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-268">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d62af-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-270">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d62af-270">The current statuses of the object.</span></span> <span data-ttu-id="d62af-271">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d62af-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d62af-272">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d62af-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-273">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-275">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="d62af-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="d62af-276">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="d62af-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d62af-277">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d62af-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d62af-278">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="d62af-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-281">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d62af-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-282">Tutte le informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="d62af-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="d62af-283">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d62af-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d62af-284">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="d62af-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-285">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-287">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d62af-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-288">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="d62af-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="d62af-289">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d62af-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="d62af-290">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d62af-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d62af-291">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d62af-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-292">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-294">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="d62af-294">Provides high level status information.</span></span> <span data-ttu-id="d62af-295">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d62af-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d62af-296">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="d62af-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d62af-297">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d62af-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d62af-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d62af-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d62af-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="d62af-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="d62af-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d62af-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d62af-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d62af-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d62af-304">)</span><span class="sxs-lookup"><span data-stu-id="d62af-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d62af-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d62af-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-306">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-308">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d62af-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="d62af-309">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d62af-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d62af-310">Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento.</span><span class="sxs-lookup"><span data-stu-id="d62af-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="d62af-311">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="d62af-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="d62af-312">In tal caso, viene utilizzato il valore 12 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="d62af-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="d62af-313">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="d62af-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="d62af-314">Valore</span><span class="sxs-lookup"><span data-stu-id="d62af-314">Value</span></span>                                                                         | <span data-ttu-id="d62af-315">Significato</span><span class="sxs-lookup"><span data-stu-id="d62af-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="d62af-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d62af-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d62af-317">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="d62af-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d62af-318">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="d62af-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-319">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d62af-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-321">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d62af-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="d62af-322">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="d62af-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d62af-323">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="d62af-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-326">Qualificatori: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="d62af-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-327">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="d62af-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="d62af-328">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d62af-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d62af-329">**Status**</span><span class="sxs-lookup"><span data-stu-id="d62af-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-332">Descrive lo stato corrente del servizio.</span><span class="sxs-lookup"><span data-stu-id="d62af-332">Describes the current status of the service.</span></span> <span data-ttu-id="d62af-333">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="d62af-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-334">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d62af-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-335">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d62af-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d62af-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-337">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d62af-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d62af-338">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="d62af-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-339">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d62af-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-342">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d62af-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-343">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d62af-343">The scoping system's creation class name.</span></span> <span data-ttu-id="d62af-344">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="d62af-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d62af-345">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d62af-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d62af-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d62af-348">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d62af-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="d62af-349">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="d62af-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="d62af-350">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="d62af-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="d62af-351">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d62af-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-352">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d62af-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-354">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d62af-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d62af-355">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d62af-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d62af-356">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d62af-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d62af-357">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d62af-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d62af-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d62af-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d62af-359">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d62af-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d62af-360">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d62af-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d62af-361">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d62af-361">Requirements</span></span>



| <span data-ttu-id="d62af-362">Requisito</span><span class="sxs-lookup"><span data-stu-id="d62af-362">Requirement</span></span> | <span data-ttu-id="d62af-363">Valore</span><span class="sxs-lookup"><span data-stu-id="d62af-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d62af-364">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62af-364">Minimum supported client</span></span><br/> | <span data-ttu-id="d62af-365">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d62af-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d62af-366">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62af-366">Minimum supported server</span></span><br/> | <span data-ttu-id="d62af-367">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d62af-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d62af-368">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d62af-368">Namespace</span></span><br/>                | <span data-ttu-id="d62af-369">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d62af-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d62af-370">MOF</span><span class="sxs-lookup"><span data-stu-id="d62af-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d62af-371"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d62af-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d62af-372">DLL</span><span class="sxs-lookup"><span data-stu-id="d62af-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d62af-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d62af-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

