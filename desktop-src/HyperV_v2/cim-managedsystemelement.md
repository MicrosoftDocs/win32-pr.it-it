---
description: CIM \_ ManagedSystemElement è la classe di base per la gerarchia degli elementi di sistema. Qualsiasi componente di un sistema può essere potenzialmente rappresentato da questa classe o dalle relative sottoclassi.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: Classe CIM_ManagedSystemElement (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232275"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="efd83-104">Classe CIM_ManagedSystemElement (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="efd83-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="efd83-105">**CIM \_ ManagedSystemElement** è la classe base per la gerarchia degli elementi di sistema.</span><span class="sxs-lookup"><span data-stu-id="efd83-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="efd83-106">Qualsiasi componente di un sistema può essere potenzialmente rappresentato da questa classe o dalle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="efd83-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd83-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efd83-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a><span data-ttu-id="efd83-108">Members</span><span class="sxs-lookup"><span data-stu-id="efd83-108">Members</span></span>

<span data-ttu-id="efd83-109">La classe **CIM \_ ManagedSystemElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="efd83-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="efd83-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efd83-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efd83-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efd83-111">Properties</span></span>

<span data-ttu-id="efd83-112">La classe **CIM \_ ManagedSystemElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="efd83-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efd83-113">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="efd83-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efd83-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efd83-116">Indica la capacità della strumentazione di comunicare con questo elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="efd83-117">Un valore **null** indica che la strumentazione non supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="efd83-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efd83-118">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efd83-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="efd83-119">**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="efd83-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="efd83-120">**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="efd83-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="efd83-121">**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="efd83-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="efd83-122">**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="efd83-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="efd83-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="efd83-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="efd83-124">**Fornitore riservato** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="efd83-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="efd83-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efd83-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-128">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**","**CIM \_ ManagedSystemElement**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="efd83-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="efd83-129">Indica informazioni aggiuntive sullo stato complementari alla proprietà **PrimaryStatus** .</span><span class="sxs-lookup"><span data-stu-id="efd83-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="efd83-130">Un valore **null** indica che la strumentazione non supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="efd83-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="efd83-131">**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="efd83-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="efd83-132">**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="efd83-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="efd83-133">**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="efd83-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="efd83-134">**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="efd83-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="efd83-135">**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="efd83-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="efd83-136">**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="efd83-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="efd83-137">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="efd83-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="efd83-138">**Fornitore riservato** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="efd83-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="efd83-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efd83-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efd83-142">Indica lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-142">Indicates the current health of the element.</span></span> <span data-ttu-id="efd83-143">Questo attributo esprime l'integrità dell'elemento, ma non necessariamente l'integrità dei sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="efd83-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efd83-144">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efd83-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="efd83-145">**OK** (5)</span><span class="sxs-lookup"><span data-stu-id="efd83-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="efd83-146">**Danneggiato/avviso** (10)</span><span class="sxs-lookup"><span data-stu-id="efd83-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="efd83-147">**Errore secondario** (15)</span><span class="sxs-lookup"><span data-stu-id="efd83-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="efd83-148">**Errore principale** (20)</span><span class="sxs-lookup"><span data-stu-id="efd83-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="efd83-149">**Errore critico** (25)</span><span class="sxs-lookup"><span data-stu-id="efd83-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="efd83-150">**Errore irreversibile** (30)</span><span class="sxs-lookup"><span data-stu-id="efd83-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="efd83-151">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="efd83-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="efd83-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-153">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="efd83-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-155">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="efd83-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="efd83-156">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="efd83-156">Indicates when the object was installed.</span></span> <span data-ttu-id="efd83-157">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="efd83-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="efd83-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="efd83-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efd83-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-161">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="efd83-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="efd83-162">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="efd83-162">The label by which the object is known.</span></span> <span data-ttu-id="efd83-163">Quando è sottoclassata, è possibile eseguire l'override della proprietà **Name** come proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="efd83-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="efd83-164">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="efd83-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efd83-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-167">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="efd83-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="efd83-168">Indica la condizione operativa corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="efd83-169">Questa proprietà può essere utilizzata per fornire informazioni più dettagliate sul valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="efd83-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="efd83-170">Un valore **null** indica che la strumentazione non supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="efd83-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="efd83-171">"Unknown" indica</span><span class="sxs-lookup"><span data-stu-id="efd83-171">"Unknown" indicates</span></span>

<span data-ttu-id="efd83-172">"None" indica che</span><span class="sxs-lookup"><span data-stu-id="efd83-172">"None" indicates that</span></span>

<span data-ttu-id="efd83-173">Manutenzione</span><span class="sxs-lookup"><span data-stu-id="efd83-173">"Servicing"</span></span>

<span data-ttu-id="efd83-174">Avvio</span><span class="sxs-lookup"><span data-stu-id="efd83-174">"Starting"</span></span>

<span data-ttu-id="efd83-175">Arresto</span><span class="sxs-lookup"><span data-stu-id="efd83-175">"Stopping"</span></span>

<span data-ttu-id="efd83-176">"Stopped" e "Aborted" sono simili, sebbene il primo, mentre il secondo i</span><span class="sxs-lookup"><span data-stu-id="efd83-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="efd83-177">"Inattivo" indica che</span><span class="sxs-lookup"><span data-stu-id="efd83-177">"Dormant" indicates that</span></span>

<span data-ttu-id="efd83-178">"Completed" indica che t</span><span class="sxs-lookup"><span data-stu-id="efd83-178">"Completed" indicates that t</span></span>

<span data-ttu-id="efd83-179">Migrazione</span><span class="sxs-lookup"><span data-stu-id="efd83-179">"Migrating"</span></span>

<span data-ttu-id="efd83-180">Immigrare</span><span class="sxs-lookup"><span data-stu-id="efd83-180">"Immigrating"</span></span>

<span data-ttu-id="efd83-181">Emigrare</span><span class="sxs-lookup"><span data-stu-id="efd83-181">"Emigrating"</span></span>

<span data-ttu-id="efd83-182">"Chiusura in corso"</span><span class="sxs-lookup"><span data-stu-id="efd83-182">"Shutting Down"</span></span>

<span data-ttu-id="efd83-183">"In test"</span><span class="sxs-lookup"><span data-stu-id="efd83-183">"In Test"</span></span>

<span data-ttu-id="efd83-184">Transizione</span><span class="sxs-lookup"><span data-stu-id="efd83-184">"Transitioning"</span></span>

<span data-ttu-id="efd83-185">"In servizio"</span><span class="sxs-lookup"><span data-stu-id="efd83-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efd83-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efd83-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-187">L'implementazione è in genere in grado di restituire questa proprietà, ma in questo momento non è in grado di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="efd83-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="efd83-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="efd83-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-189">L'implementazione (provider) è in grado di restituire un valore per questa proprietà, ma non mai per questo particolare componente hardware/software oppure la proprietà non viene intenzionalmente utilizzata perché non aggiunge informazioni significative, come nel caso di una proprietà che ha lo scopo di aggiungere informazioni aggiuntive a un'altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="efd83-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="efd83-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="efd83-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-191">Descrive un elemento configurato, mantenuto, pulito o amministrato in altro modo.</span><span class="sxs-lookup"><span data-stu-id="efd83-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="efd83-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="efd83-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-193">Descrive un elemento inizializzato.</span><span class="sxs-lookup"><span data-stu-id="efd83-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="efd83-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="efd83-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-195">Descrive un elemento che viene portato a un'interruzione ordinata.</span><span class="sxs-lookup"><span data-stu-id="efd83-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="efd83-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="efd83-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-197">Si è verificata un'interruzione corretta e ordinata.</span><span class="sxs-lookup"><span data-stu-id="efd83-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="efd83-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="efd83-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-199">Si è verificato un arresto improvviso, in cui potrebbe essere necessario aggiornare lo stato e la configurazione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="efd83-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="efd83-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-201">L'elemento è inattivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="efd83-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="efd83-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="efd83-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-203">L'elemento ha completato l'operazione.</span><span class="sxs-lookup"><span data-stu-id="efd83-203">The element has completed its operation.</span></span> <span data-ttu-id="efd83-204">Questo valore deve essere combinato con OK, Error o degradato in PrimaryStatus, in modo che un client possa stabilire se l'operazione completa è stata completata con OK (superato), completato con errore (Failed) o completato con ridotto (l'operazione è stata completata, ma non è stata completata correttamente o non è stato segnalato un errore).</span><span class="sxs-lookup"><span data-stu-id="efd83-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="efd83-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="efd83-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-206">È in corso lo spostamento dell'elemento tra gli elementi host.</span><span class="sxs-lookup"><span data-stu-id="efd83-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="efd83-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="efd83-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-208">L'elemento è stato rimosso dall'elemento host.</span><span class="sxs-lookup"><span data-stu-id="efd83-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="efd83-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="efd83-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-210">L'elemento viene spostato in un nuovo elemento host.</span><span class="sxs-lookup"><span data-stu-id="efd83-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="efd83-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="efd83-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="efd83-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="efd83-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-213">Descrive un elemento che viene portato a un arresto improvviso.</span><span class="sxs-lookup"><span data-stu-id="efd83-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="efd83-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="efd83-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-215">L'elemento sta eseguendo funzioni di test.</span><span class="sxs-lookup"><span data-stu-id="efd83-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="efd83-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="efd83-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-217">Descrive un elemento compreso tra Stati, ovvero non è completamente disponibile nello stato precedente o nello stato successivo.</span><span class="sxs-lookup"><span data-stu-id="efd83-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="efd83-218">Questo valore deve essere utilizzato se non sono applicabili altri valori che indicano una transizione a uno stato specifico.</span><span class="sxs-lookup"><span data-stu-id="efd83-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="efd83-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="efd83-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-220">Descrive un elemento in servizio e operativo.</span><span class="sxs-lookup"><span data-stu-id="efd83-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="efd83-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="efd83-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="efd83-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="efd83-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="efd83-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-224">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efd83-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="efd83-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-226">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**StatusDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="efd83-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="efd83-227">Contiene gli indicatori dello stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="efd83-228">Il primo valore della proprietà **OperationalStatus** deve contenere lo stato primario per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="efd83-229">La proprietà **OperationalStatus** sostituisce la proprietà deprecated **status** .</span><span class="sxs-lookup"><span data-stu-id="efd83-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="efd83-230">A causa dell'uso generalizzato della proprietà **status** esistente nelle applicazioni di gestione, si consiglia vivamente ai provider o alla strumentazione di fornire le proprietà **status** e **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="efd83-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="efd83-231">Quando instrumentato, **lo stato**, poiché si tratta di una proprietà a valore singolo, deve fornire anche lo stato primario dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efd83-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efd83-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="efd83-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="efd83-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="efd83-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="efd83-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="efd83-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (3)</span><span class="sxs-lookup"><span data-stu-id="efd83-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="efd83-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (4)</span><span class="sxs-lookup"><span data-stu-id="efd83-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-237">L'elemento è funzionante, ma richiede attenzione.</span><span class="sxs-lookup"><span data-stu-id="efd83-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="efd83-238">Esempi di stati "sottolineati" sono l'overload, il surriscaldamento e così via.</span><span class="sxs-lookup"><span data-stu-id="efd83-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="efd83-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (5)</span><span class="sxs-lookup"><span data-stu-id="efd83-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-240">Un elemento funziona nominalmente, ma prevede un errore nel prossimo futuro.</span><span class="sxs-lookup"><span data-stu-id="efd83-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="efd83-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (6)</span><span class="sxs-lookup"><span data-stu-id="efd83-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="efd83-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="efd83-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="efd83-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (8)</span><span class="sxs-lookup"><span data-stu-id="efd83-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="efd83-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (9)</span><span class="sxs-lookup"><span data-stu-id="efd83-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="efd83-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (10)</span><span class="sxs-lookup"><span data-stu-id="efd83-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-246">Si è verificata un'interruzione ordinata.</span><span class="sxs-lookup"><span data-stu-id="efd83-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="efd83-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (11)</span><span class="sxs-lookup"><span data-stu-id="efd83-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-248">Elemento configurato, mantenuto, pulito o amministrato in altro modo.</span><span class="sxs-lookup"><span data-stu-id="efd83-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="efd83-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)</span><span class="sxs-lookup"><span data-stu-id="efd83-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-250">Il sistema di monitoraggio conosce questo elemento, ma non è mai stato in grado di stabilire le comunicazioni con questo elemento.</span><span class="sxs-lookup"><span data-stu-id="efd83-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="efd83-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)</span><span class="sxs-lookup"><span data-stu-id="efd83-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-252">È noto che l'elemento ManagedSystem esiste ed è stato contattato correttamente in passato, ma non è attualmente raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="efd83-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="efd83-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (14)</span><span class="sxs-lookup"><span data-stu-id="efd83-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-254">Si è verificato un arresto improvviso, dove lo stato e la configurazione dell'elemento potrebbero dover essere aggiornati.</span><span class="sxs-lookup"><span data-stu-id="efd83-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="efd83-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (15)</span><span class="sxs-lookup"><span data-stu-id="efd83-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-256">L'elemento è inattivo o inattivo.</span><span class="sxs-lookup"><span data-stu-id="efd83-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="efd83-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (16)</span><span class="sxs-lookup"><span data-stu-id="efd83-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-258">Questo elemento potrebbe essere "OK" ma un altro elemento, da cui dipende, è in errore.</span><span class="sxs-lookup"><span data-stu-id="efd83-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="efd83-259">Un esempio è un servizio di rete o un endpoint che non può funzionare a causa di problemi di rete di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="efd83-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="efd83-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (17)</span><span class="sxs-lookup"><span data-stu-id="efd83-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-261">L'elemento ha completato l'operazione.</span><span class="sxs-lookup"><span data-stu-id="efd83-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="efd83-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Modalità risparmio di energia** (18)</span><span class="sxs-lookup"><span data-stu-id="efd83-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="efd83-263">L'elemento ha informazioni aggiuntive sul modello di alimentazione contenute nell'associazione PowerManagementService associata.</span><span class="sxs-lookup"><span data-stu-id="efd83-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="efd83-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="efd83-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="efd83-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="efd83-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="efd83-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efd83-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-269">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**DetailedStatus**","**CIM \_ ManagedSystemElement**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="efd83-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="efd83-270">Indica un valore di stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="efd83-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efd83-271">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efd83-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="efd83-272">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="efd83-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="efd83-273">**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="efd83-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="efd83-274">**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="efd83-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="efd83-275">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="efd83-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="efd83-276">**Fornitore riservato** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="efd83-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-277">**Status**</span><span class="sxs-lookup"><span data-stu-id="efd83-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="efd83-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efd83-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-280">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ ManagedSystemElement**.**OperationalStatus**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="efd83-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="efd83-281">Indica lo stato primario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="efd83-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="efd83-282">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="efd83-282">This property is deprecated.</span></span> <span data-ttu-id="efd83-283">Viene sostituita dalla proprietà **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="efd83-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="efd83-284">Se si sceglie di usare la proprietà **status** per la compatibilità con le versioni precedenti, è necessario che sia secondaria alla proprietà **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="efd83-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="efd83-285">("OK")</span><span class="sxs-lookup"><span data-stu-id="efd83-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-286">("Errore")</span><span class="sxs-lookup"><span data-stu-id="efd83-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-287">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="efd83-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-288">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="efd83-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-289">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="efd83-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-290">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="efd83-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-291">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="efd83-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-292">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="efd83-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-293">("Sottolineato")</span><span class="sxs-lookup"><span data-stu-id="efd83-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-294">("Non ripristino")</span><span class="sxs-lookup"><span data-stu-id="efd83-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-295">("Nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="efd83-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-296">("Comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="efd83-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="efd83-297">("Arrestato")</span><span class="sxs-lookup"><span data-stu-id="efd83-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efd83-298">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="efd83-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efd83-299">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="efd83-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="efd83-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efd83-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efd83-301">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ManagedSystemElement**.**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="efd83-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="efd83-302">Indica le descrizioni dei valori corrispondenti nella matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="efd83-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="efd83-303">Se, ad esempio, un elemento nella proprietà **OperationalStatus** contiene il valore che si **interrompe**, l'elemento in corrispondenza dello stesso indice di matrice in questa proprietà potrebbe contenere una spiegazione del motivo per cui un oggetto viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="efd83-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efd83-304">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efd83-304">Requirements</span></span>



| <span data-ttu-id="efd83-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="efd83-305">Requirement</span></span> | <span data-ttu-id="efd83-306">Valore</span><span class="sxs-lookup"><span data-stu-id="efd83-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efd83-307">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efd83-307">Minimum supported client</span></span><br/> | <span data-ttu-id="efd83-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="efd83-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="efd83-309">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efd83-309">Minimum supported server</span></span><br/> | <span data-ttu-id="efd83-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="efd83-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="efd83-311">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="efd83-311">Namespace</span></span><br/>                | <span data-ttu-id="efd83-312">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="efd83-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="efd83-313">MOF</span><span class="sxs-lookup"><span data-stu-id="efd83-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efd83-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efd83-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efd83-315">DLL</span><span class="sxs-lookup"><span data-stu-id="efd83-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efd83-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efd83-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efd83-317">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efd83-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd83-318">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="efd83-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

