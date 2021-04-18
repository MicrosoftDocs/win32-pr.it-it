---
description: "\\_L'indicazione CIM è la classe base astratta per tutte le notifiche relative alle modifiche apportate agli oggetti dello schema e ai dati degli oggetti dello schema, eventi rilevati dai provider e dalla strumentazione. Le sottoclassi dell' \\_ indicazione CIM rappresentano tipi specifici di notifiche."
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: Classe CIM_Indication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311143"
---
# <a name="cim_indication-class"></a><span data-ttu-id="74f3b-104">\_Classe di indicazione CIM</span><span class="sxs-lookup"><span data-stu-id="74f3b-104">CIM\_Indication class</span></span>

<span data-ttu-id="74f3b-105">**CIM \_ Indica** la classe di base astratta per tutte le notifiche relative alle modifiche apportate agli oggetti dello schema e ai dati degli oggetti dello schema, eventi rilevati dai provider e dalla strumentazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="74f3b-106">Le sottoclassi dell' **\_ indicazione CIM** rappresentano tipi specifici di notifiche.</span><span class="sxs-lookup"><span data-stu-id="74f3b-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f3b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74f3b-107">Syntax</span></span>

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a><span data-ttu-id="74f3b-108">Members</span><span class="sxs-lookup"><span data-stu-id="74f3b-108">Members</span></span>

<span data-ttu-id="74f3b-109">La classe di **\_ indicazione CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="74f3b-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="74f3b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74f3b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74f3b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74f3b-111">Properties</span></span>

<span data-ttu-id="74f3b-112">La classe di **\_ indicazione CIM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="74f3b-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74f3b-113">**CorrelatedIndications**</span><span class="sxs-lookup"><span data-stu-id="74f3b-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="74f3b-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-116">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Notifiche correlate "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicazione CIM**.**IndicationIdentifier**")</span><span class="sxs-lookup"><span data-stu-id="74f3b-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-117">Matrice che contiene i valori **IndicationIdentifier** delle notifiche correlate a questo.</span><span class="sxs-lookup"><span data-stu-id="74f3b-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="74f3b-118">**IndicationFilterName**</span><span class="sxs-lookup"><span data-stu-id="74f3b-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74f3b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-121">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")</span><span class="sxs-lookup"><span data-stu-id="74f3b-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-122">Identificatore del filtro di indicazione che elabora l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="74f3b-123">Il servizio di invio imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="74f3b-123">The sending service sets this property.</span></span> <span data-ttu-id="74f3b-124">Questa proprietà è correlata alla proprietà **Name** dell'oggetto **\_ IndicationFilter CIM** .</span><span class="sxs-lookup"><span data-stu-id="74f3b-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="74f3b-125">Il valore di **IndicationFilterName** deve usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="74f3b-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="74f3b-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="74f3b-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="74f3b-127">*<OrgID>* deve includere un nome con copyright, marchio o univoco di proprietà dell'entità di business a cui appartiene l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74f3b-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="74f3b-128">*<OrgID>* non devono contenere i due punti (:)</span><span class="sxs-lookup"><span data-stu-id="74f3b-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="74f3b-129">*<LocalID>* Identificatore univoco scelto dall'entità di business a cui appartiene l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74f3b-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="74f3b-130">**IndicationIdentifier**</span><span class="sxs-lookup"><span data-stu-id="74f3b-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74f3b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-133">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Identificatore notifica ")</span><span class="sxs-lookup"><span data-stu-id="74f3b-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-134">Identificatore dell'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-134">An identifier of the indication.</span></span> <span data-ttu-id="74f3b-135">Questa proprietà può essere usata come valore chiave nella matrice di proprietà **CorrelatedIndications** .</span><span class="sxs-lookup"><span data-stu-id="74f3b-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="74f3b-136">Pertanto, **IndicationIdentifier** deve essere un valore univoco all'interno dello spazio dei nomi di questa istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="74f3b-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="74f3b-137">Per assicurarsi che **IndicationIdentifier** sia univoco, deve usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="74f3b-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="74f3b-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="74f3b-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="74f3b-139">*<OrgID>* deve includere un nome con copyright, marchio o univoco di proprietà dell'entità di business a cui appartiene l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74f3b-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="74f3b-140">*<OrgID>* non devono contenere i due punti (:)</span><span class="sxs-lookup"><span data-stu-id="74f3b-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="74f3b-141">*<LocalID>* Identificatore univoco scelto dall'entità di business a cui appartiene l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="74f3b-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="74f3b-142">Per le istanze definite da DMTF, *<OrgID>* deve essere impostato su "CIM".</span><span class="sxs-lookup"><span data-stu-id="74f3b-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="74f3b-143">**IndicationTime**</span><span class="sxs-lookup"><span data-stu-id="74f3b-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-144">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74f3b-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-146">Data e ora di creazione dell'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-146">The time and date when the indication was created.</span></span> <span data-ttu-id="74f3b-147">La proprietà può essere impostata su **null** se l'entità che ha creato l'indicazione non è in grado di determinare tali informazioni.</span><span class="sxs-lookup"><span data-stu-id="74f3b-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="74f3b-148">Il valore **IndicationTime** può essere lo stesso per le indicazioni generate in rapida successione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="74f3b-149">**OtherSeverity**</span><span class="sxs-lookup"><span data-stu-id="74f3b-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74f3b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-152">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span><span class="sxs-lookup"><span data-stu-id="74f3b-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-153">Gravità dell'indicazione dal punto di vista del notificatore quando **PerceivedSeverity** è impostato su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="74f3b-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="74f3b-154">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="74f3b-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74f3b-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-157">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravità percepita ")</span><span class="sxs-lookup"><span data-stu-id="74f3b-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-158">Gravità dell'indicazione dal punto di vista del notificatore.</span><span class="sxs-lookup"><span data-stu-id="74f3b-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74f3b-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="74f3b-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-160">la gravità percepita dell'indicazione è sconosciuta o indeterminata.</span><span class="sxs-lookup"><span data-stu-id="74f3b-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74f3b-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="74f3b-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-162">Indica che il valore della gravità è reperibile nella proprietà **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="74f3b-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="74f3b-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)</span><span class="sxs-lookup"><span data-stu-id="74f3b-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-164">Quando si fornisce una risposta informativa, è necessario utilizzare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="74f3b-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="74f3b-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/avviso** (3)</span><span class="sxs-lookup"><span data-stu-id="74f3b-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-166">Deve essere usato quando è appropriato per consentire all'utente di decidere se è necessaria un'azione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="74f3b-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secondario** (4)</span><span class="sxs-lookup"><span data-stu-id="74f3b-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-168">L'azione è necessaria, ma in questo momento la situazione non è grave.</span><span class="sxs-lookup"><span data-stu-id="74f3b-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="74f3b-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principale** (5)</span><span class="sxs-lookup"><span data-stu-id="74f3b-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-170">L'azione è ora necessaria.</span><span class="sxs-lookup"><span data-stu-id="74f3b-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="74f3b-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (6)</span><span class="sxs-lookup"><span data-stu-id="74f3b-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-172">L'azione è ora necessaria e l'ambito è ampio (probabilmente verrà generata un'interruzione imminente a una risorsa critica).</span><span class="sxs-lookup"><span data-stu-id="74f3b-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="74f3b-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irreversibile/irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="74f3b-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="74f3b-174">si è verificato un errore, ma è troppo tardi per intraprendere un'azione correttiva.</span><span class="sxs-lookup"><span data-stu-id="74f3b-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="74f3b-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="74f3b-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74f3b-176">**SequenceContext**</span><span class="sxs-lookup"><span data-stu-id="74f3b-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="74f3b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-179">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicazione CIM**.**SequenceNumber**")</span><span class="sxs-lookup"><span data-stu-id="74f3b-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-180">Contesto di sequenza dell'identificatore di sequenza per l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="74f3b-181">Se un servizio non supporta gli identificatori di sequenza per le indicazioni, questa proprietà deve essere impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="74f3b-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="74f3b-182">Se l'indicazione viene recapitata, questa proprietà rimane invariata.</span><span class="sxs-lookup"><span data-stu-id="74f3b-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="74f3b-183">L'identificatore di sequenza per l'indicazione consente a un listener di identificare le indicazioni duplicate quando il servizio tenta di recapitare le indicazioni, riordinare le indicazioni che non arrivano in ordine e rilevare le indicazioni perse.</span><span class="sxs-lookup"><span data-stu-id="74f3b-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="74f3b-184">Per assicurarsi che **SequenceContext** sia univoco, deve usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="74f3b-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="74f3b-185">nome-servizio *-indicazione* \# *CIM-Service-Start-ID* \# *listener-destinazione-fase di creazione*</span><span class="sxs-lookup"><span data-stu-id="74f3b-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="74f3b-186">*indication-Service-Name* è il valore della proprietà **Name** dell'istanza **CIM \_ IndicationService** che fornisce l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="74f3b-187">*CIM-Service-Start-ID* è un identificatore che identifica in modo univoco l'operazione di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="74f3b-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="74f3b-188">Ad esempio, potrebbe trattarsi di un timestamp dell'ora di inizio o di un contatore che aumenta per ogni avvio o riavvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="74f3b-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="74f3b-189">*listener-Destination-Creation-Time* è un timestamp dell'ora di creazione dell'istanza **CIM \_ ListenerDestination** che rappresenta la destinazione del listener. nSince questo formato è solo una raccomandazione, i client CIM devono trattare il valore come un identificatore opaco per il contesto della sequenza e non deve basarsi su questo formato.</span><span class="sxs-lookup"><span data-stu-id="74f3b-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="74f3b-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="74f3b-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74f3b-191">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="74f3b-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="74f3b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74f3b-193">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicazione CIM**.**SequenceContext**")</span><span class="sxs-lookup"><span data-stu-id="74f3b-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="74f3b-194">Numero di sequenza dell'identificatore di sequenza per l'indicazione.</span><span class="sxs-lookup"><span data-stu-id="74f3b-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="74f3b-195">L'identificatore di sequenza per l'indicazione consente a un listener di identificare le indicazioni duplicate quando il servizio tenta di recapitare le indicazioni, riordinare le indicazioni che non arrivano in ordine e rilevare le indicazioni perse.</span><span class="sxs-lookup"><span data-stu-id="74f3b-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="74f3b-196">Il numero di sequenza presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="74f3b-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="74f3b-197">Il numero di sequenza viene reimpostato su "0" ogni volta che viene modificato il valore di **SequenceContext** .</span><span class="sxs-lookup"><span data-stu-id="74f3b-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="74f3b-198">Ogni volta che la destinazione del listener riceve una nuova indicazione, il numero di sequenza viene aumentato di "1".</span><span class="sxs-lookup"><span data-stu-id="74f3b-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="74f3b-199">Il numero di sequenza viene eseguito a capo a "0" quando viene superato l'intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="74f3b-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="74f3b-200">Se l'indicazione viene recapitata, il **SequenceNumber** rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="74f3b-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74f3b-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74f3b-201">Requirements</span></span>



| <span data-ttu-id="74f3b-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="74f3b-202">Requirement</span></span> | <span data-ttu-id="74f3b-203">Valore</span><span class="sxs-lookup"><span data-stu-id="74f3b-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f3b-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74f3b-204">Minimum supported client</span></span><br/> | <span data-ttu-id="74f3b-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="74f3b-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="74f3b-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74f3b-206">Minimum supported server</span></span><br/> | <span data-ttu-id="74f3b-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="74f3b-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="74f3b-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74f3b-208">Namespace</span></span><br/>                | <span data-ttu-id="74f3b-209">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="74f3b-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74f3b-210">MOF</span><span class="sxs-lookup"><span data-stu-id="74f3b-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74f3b-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74f3b-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74f3b-212">DLL</span><span class="sxs-lookup"><span data-stu-id="74f3b-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74f3b-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74f3b-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74f3b-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74f3b-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f3b-215">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="74f3b-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

