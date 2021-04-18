---
description: I qualificatori facoltativi indirizzano situazioni ricorrenti non comuni a tutte le implementazioni conformi a CIM, che non sono necessarie per interpretare questi qualificatori.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Qualificatori facoltativi
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318181"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="67a63-103">Qualificatori facoltativi</span><span class="sxs-lookup"><span data-stu-id="67a63-103">Optional Qualifiers</span></span>

<span data-ttu-id="67a63-104">I qualificatori facoltativi indirizzano situazioni ricorrenti non comuni a tutte le implementazioni conformi a CIM, che non sono necessarie per interpretare questi qualificatori.</span><span class="sxs-lookup"><span data-stu-id="67a63-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="67a63-105">I qualificatori facoltativi sono forniti nella specifica per evitare qualificatori definiti dall'utente casuali che possono verificarsi in queste situazioni ricorrenti.</span><span class="sxs-lookup"><span data-stu-id="67a63-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="67a63-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Eliminare**</span><span class="sxs-lookup"><span data-stu-id="67a63-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-107">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-107">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-108">Si applica a: associazioni, riferimenti</span><span class="sxs-lookup"><span data-stu-id="67a63-108">Applies to: associations, references</span></span>

<span data-ttu-id="67a63-109">Per le associazioni, indica se l'associazione qualificata deve essere eliminata se uno degli oggetti a cui viene fatto riferimento nell'associazione viene eliminato e se il rispettivo oggetto a cui viene fatto riferimento nell'associazione viene qualificato con **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="67a63-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="67a63-110">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="67a63-110">The default is **FALSE**.</span></span>

<span data-ttu-id="67a63-111">Per i riferimenti, questo qualificatore indica se l'oggetto a cui si fa riferimento deve essere eliminato se l'associazione contenente il riferimento viene eliminata e qualificata con **IfDeleted** oppure se uno degli oggetti a cui viene fatto riferimento nell'associazione viene eliminato e il rispettivo oggetto a cui viene fatto riferimento nell'associazione viene qualificato con **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="67a63-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="67a63-112">Utilizzo: le applicazioni devono tenere traccia delle associazioni e dei riferimenti contrassegnati con il qualificatore **Delete** ed eliminare l'associazione o il riferimento in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="67a63-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="67a63-113">Se un oggetto nell'associazione è stato eliminato ma non è contrassegnato con **IfDeleted**, l'associazione non deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="67a63-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="67a63-114">Questa regola di utilizzo deve essere verificata quando viene definito il modello di sicurezza CIM.</span><span class="sxs-lookup"><span data-stu-id="67a63-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Costoso**</span><span class="sxs-lookup"><span data-stu-id="67a63-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-116">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-117">Si applica a: proprietà, riferimenti, classi, associazioni, metodi</span><span class="sxs-lookup"><span data-stu-id="67a63-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="67a63-118">Indica se l'azione implicita richiede un calcolo esteso.</span><span class="sxs-lookup"><span data-stu-id="67a63-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="67a63-119">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="67a63-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span><span class="sxs-lookup"><span data-stu-id="67a63-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-121">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-121">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-122">Si applica a: associazioni e riferimenti</span><span class="sxs-lookup"><span data-stu-id="67a63-122">Applies to: associations and references</span></span>

<span data-ttu-id="67a63-123">Indica se è necessario eliminare tutti gli oggetti all'interno di un'associazione qualificata da **Delete** se l'oggetto a cui si fa riferimento o l'associazione viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="67a63-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="67a63-124">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="67a63-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indicizzata**</span><span class="sxs-lookup"><span data-stu-id="67a63-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-126">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-127">Si applica a: proprietà, metodi</span><span class="sxs-lookup"><span data-stu-id="67a63-127">Applies to: properties, methods</span></span>

<span data-ttu-id="67a63-128">Indica se una proprietà della classe deve essere indicizzata.</span><span class="sxs-lookup"><span data-stu-id="67a63-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="67a63-129">Quando viene applicato alle proprietà nelle classi ospitate dal repository, questo ha il significato di creare (al momento della creazione della classe) una ricerca di query secondaria veloce per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="67a63-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="67a63-130">È consentito solo il valore **true** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="67a63-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisibile**</span><span class="sxs-lookup"><span data-stu-id="67a63-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-132">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-132">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-133">Si applica a: associazioni, proprietà, metodi, riferimenti, classi</span><span class="sxs-lookup"><span data-stu-id="67a63-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="67a63-134">Indica se l'associazione viene definita solo per scopi interni (ad esempio, per la definizione della semantica delle dipendenze) e non deve essere visualizzata, ad esempio in maps.</span><span class="sxs-lookup"><span data-stu-id="67a63-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="67a63-135">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="67a63-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Grandi dimensioni**</span><span class="sxs-lookup"><span data-stu-id="67a63-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-137">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-138">Si applica a: proprietà, classi</span><span class="sxs-lookup"><span data-stu-id="67a63-138">Applies to: properties, classes</span></span>

<span data-ttu-id="67a63-139">Indica se la proprietà o la classe richiede una grande quantità di spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="67a63-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="67a63-140">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="67a63-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not \_ null**</span><span class="sxs-lookup"><span data-stu-id="67a63-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-142">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-143">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="67a63-143">Applies to: properties</span></span>

<span data-ttu-id="67a63-144">Indica se una proprietà di classe non può assumere un valore **null** (**VT \_ null**).</span><span class="sxs-lookup"><span data-stu-id="67a63-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="67a63-145">È consentito solo il valore **true** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="67a63-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="67a63-146">Se questo qualificatore viene specificato, WMI non consente la creazione di istanze con la proprietà impostata su **null**, mentre le proprietà **null** restituiscono il codice di errore di **WBEM \_ E \_ \_ null non valido** .</span><span class="sxs-lookup"><span data-stu-id="67a63-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="67a63-147">Si noti che la [**chiave**](standard-qualifiers.md) e i qualificatori **indicizzati** implicano già questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="67a63-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span><span class="sxs-lookup"><span data-stu-id="67a63-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="67a63-149">Data type: **string**</span></span>

<span data-ttu-id="67a63-150">Si applica a: any</span><span class="sxs-lookup"><span data-stu-id="67a63-150">Applies to: Any</span></span>

<span data-ttu-id="67a63-151">Indica che l'elemento dello schema è dinamico e quindi popolato da un provider.</span><span class="sxs-lookup"><span data-stu-id="67a63-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="67a63-152">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="67a63-152">The default is **NULL**.</span></span> <span data-ttu-id="67a63-153">Questo qualificatore è un handle specifico dell'implementazione per la strumentazione.</span><span class="sxs-lookup"><span data-stu-id="67a63-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Sperimentale**</span><span class="sxs-lookup"><span data-stu-id="67a63-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-155">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="67a63-155">Data type: **boolean**</span></span>

<span data-ttu-id="67a63-156">Si applica a: any</span><span class="sxs-lookup"><span data-stu-id="67a63-156">Applies to: any</span></span>

<span data-ttu-id="67a63-157">Indica che l'elemento specificato è stato proposto come parte di una versione futura degli schemi CIM, ma non fa ancora parte dello schema standard.</span><span class="sxs-lookup"><span data-stu-id="67a63-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="67a63-158">L'elemento è invece disponibile per consentire agli utenti di sperimentare, implementare e fornire commenti e suggerimenti su.</span><span class="sxs-lookup"><span data-stu-id="67a63-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="67a63-159">In base ai commenti e suggerimenti, l'elemento può essere aggiunto allo standard come presentato, modificato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="67a63-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="67a63-160">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="67a63-160">The default is **FALSE**.</span></span> <span data-ttu-id="67a63-161">Non è necessario che un'implementazione supporti un elemento con questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="67a63-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="67a63-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="67a63-163">Data type: **string**</span></span>

<span data-ttu-id="67a63-164">Si applica a: proprietà, riferimenti, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="67a63-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="67a63-165">Tipo specifico assegnato a un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="67a63-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="67a63-166">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="67a63-166">The default is **NULL**.</span></span>

<span data-ttu-id="67a63-167">Utilizzo: è necessario usare il qualificatore **SyntaxType** con questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="67a63-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span><span class="sxs-lookup"><span data-stu-id="67a63-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="67a63-169">Data type: **string**</span></span>

<span data-ttu-id="67a63-170">Si applica a: proprietà, riferimenti, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="67a63-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="67a63-171">Formato del qualificatore di **sintassi** .</span><span class="sxs-lookup"><span data-stu-id="67a63-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="67a63-172">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="67a63-172">The default is **NULL**.</span></span>

<span data-ttu-id="67a63-173">Utilizzo: è necessario usare il qualificatore della **sintassi** con questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="67a63-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="67a63-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="67a63-175">Data type: **string**</span></span>

<span data-ttu-id="67a63-176">Si applica a: classi, proprietà, metodi, associazioni, indicazioni, riferimenti</span><span class="sxs-lookup"><span data-stu-id="67a63-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="67a63-177">Circostanze in cui viene attivato un trigger.</span><span class="sxs-lookup"><span data-stu-id="67a63-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="67a63-178">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="67a63-178">The default is **NULL**.</span></span> <span data-ttu-id="67a63-179">I tipi di trigger variano in base al costrutto di Metamodello.</span><span class="sxs-lookup"><span data-stu-id="67a63-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="67a63-180">Per le classi e le associazioni, i valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="67a63-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="67a63-181">Create</span><span class="sxs-lookup"><span data-stu-id="67a63-181">Create</span></span>

<span data-ttu-id="67a63-182">Delete</span><span class="sxs-lookup"><span data-stu-id="67a63-182">Delete</span></span>

<span data-ttu-id="67a63-183">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="67a63-183">Update</span></span>

<span data-ttu-id="67a63-184">Access</span><span class="sxs-lookup"><span data-stu-id="67a63-184">Access</span></span>

<span data-ttu-id="67a63-185">Per le proprietà e i riferimenti, i valori validi sono: Update e Access.</span><span class="sxs-lookup"><span data-stu-id="67a63-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="67a63-186">Per i metodi, i valori validi sono before e After.</span><span class="sxs-lookup"><span data-stu-id="67a63-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="67a63-187">Per le indicazioni, viene generato il valore valido.</span><span class="sxs-lookup"><span data-stu-id="67a63-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span><span class="sxs-lookup"><span data-stu-id="67a63-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-189">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="67a63-189">Data type: **string array**</span></span>

<span data-ttu-id="67a63-190">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="67a63-190">Applies to: properties</span></span>

<span data-ttu-id="67a63-191">Set di valori che indica che il valore della proprietà associata è sconosciuto (la proprietà non può essere considerata come avente un valore valido o significativo).</span><span class="sxs-lookup"><span data-stu-id="67a63-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="67a63-192">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="67a63-192">The default is **NULL**.</span></span>

<span data-ttu-id="67a63-193">Le convenzioni e le restrizioni usate per la definizione di valori sconosciuti sono le stesse applicabili al qualificatore [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="67a63-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="67a63-194">Si noti che non è possibile eseguire l'override di questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="67a63-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="67a63-195">Non è ragionevole consentire a una sottoclasse di trattare un valore come valore noto quando viene considerato sconosciuto da una classe padre.</span><span class="sxs-lookup"><span data-stu-id="67a63-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="67a63-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span><span class="sxs-lookup"><span data-stu-id="67a63-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="67a63-197">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="67a63-197">Data type: **string array**</span></span>

<span data-ttu-id="67a63-198">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="67a63-198">Applies to: properties</span></span>

<span data-ttu-id="67a63-199">Set di valori che indica che il valore della proprietà associata non è supportato (la proprietà non può essere considerata come avente un valore valido o significativo).</span><span class="sxs-lookup"><span data-stu-id="67a63-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="67a63-200">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="67a63-200">The default is **NULL**.</span></span>

<span data-ttu-id="67a63-201">Le convenzioni e le restrizioni usate per la definizione di valori non supportati sono le stesse applicabili al qualificatore [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="67a63-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="67a63-202">Nota non è possibile eseguire l'override di questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="67a63-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="67a63-203">Non è ragionevole consentire a una sottoclasse di trattare un valore come valore supportato considerato sconosciuto da una classe padre.</span><span class="sxs-lookup"><span data-stu-id="67a63-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67a63-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67a63-204">Requirements</span></span>



| <span data-ttu-id="67a63-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a63-205">Requirement</span></span> | <span data-ttu-id="67a63-206">Valore</span><span class="sxs-lookup"><span data-stu-id="67a63-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="67a63-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a63-207">Minimum supported client</span></span><br/> | <span data-ttu-id="67a63-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67a63-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="67a63-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a63-209">Minimum supported server</span></span><br/> | <span data-ttu-id="67a63-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67a63-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67a63-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67a63-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a63-212">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="67a63-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="67a63-213">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="67a63-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




