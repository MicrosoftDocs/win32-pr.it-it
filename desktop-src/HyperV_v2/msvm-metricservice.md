---
description: Offre la possibilità di gestire le metriche.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318332"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="7b22e-103">\_Classe MSVM MetricService</span><span class="sxs-lookup"><span data-stu-id="7b22e-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="7b22e-104">Offre la possibilità di gestire le metriche.</span><span class="sxs-lookup"><span data-stu-id="7b22e-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="7b22e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7b22e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b22e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b22e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="7b22e-107">Members</span><span class="sxs-lookup"><span data-stu-id="7b22e-107">Members</span></span>

<span data-ttu-id="7b22e-108">La **classe \_ MetricService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7b22e-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="7b22e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="7b22e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b22e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b22e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b22e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7b22e-111">Methods</span></span>

<span data-ttu-id="7b22e-112">La **classe \_ MetricService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7b22e-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="7b22e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="7b22e-113">Method</span></span>                                                                    | <span data-ttu-id="7b22e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b22e-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b22e-115">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="7b22e-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="7b22e-116">Usato per controllare la raccolta di metriche per un elemento o elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="7b22e-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="7b22e-117">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="7b22e-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="7b22e-118">Controlla la metrica in base alla classe.</span><span class="sxs-lookup"><span data-stu-id="7b22e-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="7b22e-119">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="7b22e-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="7b22e-120">Imposta i tempi di campionamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="7b22e-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="7b22e-121">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="7b22e-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="7b22e-122">Recupera i valori della metrica.</span><span class="sxs-lookup"><span data-stu-id="7b22e-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="7b22e-123">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="7b22e-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="7b22e-124">Modifica i dati dell'impostazione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b22e-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="7b22e-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7b22e-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="7b22e-126">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="7b22e-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="7b22e-127">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="7b22e-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="7b22e-128">Mostra la metrica specificata.</span><span class="sxs-lookup"><span data-stu-id="7b22e-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="7b22e-129">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="7b22e-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="7b22e-130">Mostra le metriche per classe.</span><span class="sxs-lookup"><span data-stu-id="7b22e-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="7b22e-131">**StartService**</span><span class="sxs-lookup"><span data-stu-id="7b22e-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="7b22e-132">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b22e-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="7b22e-133">**StopService**</span><span class="sxs-lookup"><span data-stu-id="7b22e-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="7b22e-134">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b22e-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="7b22e-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b22e-135">Properties</span></span>

<span data-ttu-id="7b22e-136">La **classe \_ MetricService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b22e-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b22e-137">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="7b22e-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-138">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-140">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="7b22e-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="7b22e-141">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b22e-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-142">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7b22e-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-145">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b22e-145">A short description of the object.</span></span> <span data-ttu-id="7b22e-146">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="7b22e-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7b22e-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-150">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="7b22e-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7b22e-151">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7b22e-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7b22e-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7b22e-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7b22e-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7b22e-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="7b22e-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="7b22e-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="7b22e-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="7b22e-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7b22e-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7b22e-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7b22e-160">)</span><span class="sxs-lookup"><span data-stu-id="7b22e-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b22e-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b22e-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-164">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="7b22e-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7b22e-165">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ MetricService".</span><span class="sxs-lookup"><span data-stu-id="7b22e-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-166">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7b22e-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-169">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7b22e-169">A description of the object.</span></span> <span data-ttu-id="7b22e-170">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "fornisce la gestione WMI della metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="7b22e-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7b22e-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-174">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="7b22e-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7b22e-175">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7b22e-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7b22e-176">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7b22e-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7b22e-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="7b22e-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="7b22e-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="7b22e-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="7b22e-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="7b22e-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="7b22e-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7b22e-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7b22e-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7b22e-185">)</span><span class="sxs-lookup"><span data-stu-id="7b22e-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b22e-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7b22e-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-189">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b22e-189">A display name for the object.</span></span> <span data-ttu-id="7b22e-190">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="7b22e-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-191">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="7b22e-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-192">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-194">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7b22e-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7b22e-195">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="7b22e-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7b22e-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-199">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7b22e-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="7b22e-200">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="7b22e-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="7b22e-201">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="7b22e-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7b22e-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-203">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-205">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7b22e-205">The current health of the element.</span></span> <span data-ttu-id="7b22e-206">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7b22e-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7b22e-207">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="7b22e-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7b22e-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="7b22e-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b22e-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-210">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b22e-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-212">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b22e-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="7b22e-213">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7b22e-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b22e-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-217">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7b22e-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-218">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7b22e-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7b22e-219">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7b22e-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-220">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7b22e-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-223">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="7b22e-223">The label by which the object is known.</span></span> <span data-ttu-id="7b22e-224">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "metricsvc".</span><span class="sxs-lookup"><span data-stu-id="7b22e-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-225">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7b22e-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-226">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-228">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7b22e-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7b22e-229">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7b22e-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7b22e-230">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7b22e-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7b22e-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7b22e-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="7b22e-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="7b22e-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="7b22e-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="7b22e-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="7b22e-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="7b22e-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="7b22e-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="7b22e-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="7b22e-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="7b22e-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="7b22e-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="7b22e-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="7b22e-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="7b22e-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="7b22e-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="7b22e-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7b22e-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7b22e-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7b22e-250">)</span><span class="sxs-lookup"><span data-stu-id="7b22e-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b22e-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7b22e-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-252">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-254">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b22e-254">The current statuses of the object.</span></span> <span data-ttu-id="7b22e-255">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="7b22e-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-256">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7b22e-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-259">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7b22e-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="7b22e-260">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="7b22e-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7b22e-261">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7b22e-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-262">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="7b22e-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-265">Valore che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="7b22e-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="7b22e-266">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7b22e-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-267">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="7b22e-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-270">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="7b22e-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="7b22e-271">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b22e-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="7b22e-272">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7b22e-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-273">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7b22e-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-274">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-276">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="7b22e-276">Provides high level status information.</span></span> <span data-ttu-id="7b22e-277">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7b22e-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7b22e-278">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7b22e-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7b22e-279">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7b22e-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7b22e-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7b22e-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="7b22e-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="7b22e-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="7b22e-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7b22e-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7b22e-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7b22e-286">)</span><span class="sxs-lookup"><span data-stu-id="7b22e-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b22e-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7b22e-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-288">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-290">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="7b22e-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="7b22e-291">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="7b22e-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="7b22e-292">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="7b22e-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="7b22e-293">Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="7b22e-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="7b22e-294">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="7b22e-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="7b22e-295">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="7b22e-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-296">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="7b22e-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-297">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7b22e-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-299">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7b22e-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="7b22e-300">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="7b22e-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-301">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="7b22e-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-304">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="7b22e-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="7b22e-305">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7b22e-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-306">**Status**</span><span class="sxs-lookup"><span data-stu-id="7b22e-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-309">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="7b22e-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-310">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7b22e-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-311">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7b22e-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-313">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7b22e-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7b22e-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e le stringhe sono sempre impostate su "OK".</span><span class="sxs-lookup"><span data-stu-id="7b22e-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-315">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b22e-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-318">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7b22e-318">The scoping system's creation class name.</span></span> <span data-ttu-id="7b22e-319">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="7b22e-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-320">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7b22e-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b22e-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-323">Nome del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="7b22e-323">The name of the hosting computer system.</span></span> <span data-ttu-id="7b22e-324">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="7b22e-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-325">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7b22e-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-326">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b22e-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-328">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7b22e-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7b22e-329">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b22e-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7b22e-330">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="7b22e-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b22e-331">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b22e-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b22e-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b22e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b22e-333">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7b22e-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7b22e-334">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b22e-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b22e-335">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b22e-335">Requirements</span></span>



| <span data-ttu-id="7b22e-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b22e-336">Requirement</span></span> | <span data-ttu-id="7b22e-337">Valore</span><span class="sxs-lookup"><span data-stu-id="7b22e-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b22e-338">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b22e-338">Minimum supported client</span></span><br/> | <span data-ttu-id="7b22e-339">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7b22e-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7b22e-340">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b22e-340">Minimum supported server</span></span><br/> | <span data-ttu-id="7b22e-341">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7b22e-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b22e-342">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b22e-342">Namespace</span></span><br/>                | <span data-ttu-id="7b22e-343">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b22e-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7b22e-344">MOF</span><span class="sxs-lookup"><span data-stu-id="7b22e-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b22e-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b22e-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b22e-346">DLL</span><span class="sxs-lookup"><span data-stu-id="7b22e-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b22e-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b22e-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

