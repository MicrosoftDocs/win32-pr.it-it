---
description: Tutte le implementazioni conformi a CIM devono gestire un set standard di qualificatori.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Qualificatori standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309877"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="d2501-103">Qualificatori standard</span><span class="sxs-lookup"><span data-stu-id="d2501-103">Standard Qualifiers</span></span>

<span data-ttu-id="d2501-104">Tutte le implementazioni conformi a CIM devono gestire un set standard di qualificatori.</span><span class="sxs-lookup"><span data-stu-id="d2501-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="d2501-105">Per tutti gli oggetti specifici non sono elencati tutti i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="d2501-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="d2501-106">In genere, le classi di estensione forniscono qualificatori aggiuntivi per facilitare il provisioning di istanze di classe e altre operazioni sulla classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="d2501-107">È responsabilità del provider applicare i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="d2501-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="d2501-108">WMI non impone i qualificatori, ma li utilizza solo per informare l'utente sulla modalità di utilizzo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2501-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="d2501-109">WMI è conforme alla specifica CIM 2,5.</span><span class="sxs-lookup"><span data-stu-id="d2501-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="d2501-110">I qualificatori hanno le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2501-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="d2501-111">Non tutti i qualificatori standard possono essere usati insieme.</span><span class="sxs-lookup"><span data-stu-id="d2501-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="d2501-112">Non tutti i qualificatori possono essere applicati a tutti i costrutti, ad esempio l'associazione o il riferimento.</span><span class="sxs-lookup"><span data-stu-id="d2501-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="d2501-113">Queste limitazioni sono identificate nell'elenco si applica a.</span><span class="sxs-lookup"><span data-stu-id="d2501-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="d2501-114">Per un costrutto specifico, ad esempio un'associazione o un riferimento, l'utilizzo dei qualificatori legali può essere ulteriormente vincolato perché alcuni qualificatori si escludono a vicenda, l'utilizzo di un qualificatore può implicare alcune restrizioni sul valore di un altro e così via.</span><span class="sxs-lookup"><span data-stu-id="d2501-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="d2501-115">Queste regole di utilizzo sono documentate.</span><span class="sxs-lookup"><span data-stu-id="d2501-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="d2501-116">I qualificatori legali vengono ereditati solo da entità quali proprietà, metodi, istanze o sottoclassi, non da associazioni o riferimenti.</span><span class="sxs-lookup"><span data-stu-id="d2501-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="d2501-117">Ad esempio, il qualificatore **maxlen** che si applica alle proprietà non viene ereditato dai riferimenti.</span><span class="sxs-lookup"><span data-stu-id="d2501-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="d2501-118">Di seguito sono elencati i qualificatori standard WMI.</span><span class="sxs-lookup"><span data-stu-id="d2501-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="d2501-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Astratta**</span><span class="sxs-lookup"><span data-stu-id="d2501-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-120">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-121">Si applica a: classi, associazioni, indicazioni</span><span class="sxs-lookup"><span data-stu-id="d2501-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="d2501-122">Indica se la classe è astratta e funge solo da base per le nuove classi.</span><span class="sxs-lookup"><span data-stu-id="d2501-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="d2501-123">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-123">The default is **FALSE**.</span></span> <span data-ttu-id="d2501-124">Non è possibile creare istanze di classi astratte.</span><span class="sxs-lookup"><span data-stu-id="d2501-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="d2501-125">L'assenza di questo qualificatore indica che la classe non è astratta; Pertanto, questo qualificatore è obbligatorio per tutte le classi astratte.</span><span class="sxs-lookup"><span data-stu-id="d2501-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregazione**</span><span class="sxs-lookup"><span data-stu-id="d2501-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-127">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-128">Si applica a: riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-128">Applies to: references</span></span>

<span data-ttu-id="d2501-129">Indica se il riferimento è il componente padre di un'associazione di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="d2501-130">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-130">The default is **FALSE**.</span></span>

<span data-ttu-id="d2501-131">Utilizzo: i **qualificatori aggregazione e** **aggregazione** vengono   **utilizzati insieme per** qualificare l'associazione e il riferimento padre viene specificato dall' **aggregazione** .</span><span class="sxs-lookup"><span data-stu-id="d2501-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregazione**</span><span class="sxs-lookup"><span data-stu-id="d2501-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-133">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-134">Si applica a: associazioni</span><span class="sxs-lookup"><span data-stu-id="d2501-134">Applies to: associations</span></span>

<span data-ttu-id="d2501-135">Indica se l'associazione è un'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="d2501-136">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-136">The default is **FALSE**.</span></span> <span data-ttu-id="d2501-137">Utilizzato con l' **aggregazione**.</span><span class="sxs-lookup"><span data-stu-id="d2501-137">Used with **Aggregate**.</span></span> <span data-ttu-id="d2501-138">Questo qualificatore è obbligatorio per tutte le associazioni di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span><span class="sxs-lookup"><span data-stu-id="d2501-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-140">Data type: **string**</span></span>

<span data-ttu-id="d2501-141">Si applica a: proprietà, riferimenti, metodi</span><span class="sxs-lookup"><span data-stu-id="d2501-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="d2501-142">Nome alternativo per una proprietà o un metodo nello schema.</span><span class="sxs-lookup"><span data-stu-id="d2501-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="d2501-143">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="d2501-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-145">Data type: **string**</span></span>

<span data-ttu-id="d2501-146">Si applica a: proprietà, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="d2501-147">Tipo della matrice qualificata.</span><span class="sxs-lookup"><span data-stu-id="d2501-147">Type of the qualified array.</span></span>

<span data-ttu-id="d2501-148">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="d2501-148">Valid values are:</span></span>

-   <span data-ttu-id="d2501-149">contenitore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2501-149">bag (default)</span></span>
-   <span data-ttu-id="d2501-150">indicizzati</span><span class="sxs-lookup"><span data-stu-id="d2501-150">indexed</span></span>
-   <span data-ttu-id="d2501-151">ordered</span><span class="sxs-lookup"><span data-stu-id="d2501-151">ordered</span></span>

<span data-ttu-id="d2501-152">Utilizzo: applicare questo tipo di qualificatore solo a proprietà e parametri che sono matrici (definite mediante la sintassi della parentesi quadre).</span><span class="sxs-lookup"><span data-stu-id="d2501-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="d2501-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span><span class="sxs-lookup"><span data-stu-id="d2501-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-154">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2501-154">Data type: **string array**</span></span>

<span data-ttu-id="d2501-155">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-156">Mappa di posizioni di bit significative in cui ogni posizione significativa può essere "on" o "off".</span><span class="sxs-lookup"><span data-stu-id="d2501-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="d2501-157">Ogni bit "on" viene mappato a un valore corrispondente nella matrice **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="d2501-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="d2501-158">Se si dispone di più bit "on", vengono indicati più valori simultanei nella matrice **BitValues** .</span><span class="sxs-lookup"><span data-stu-id="d2501-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="d2501-159">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-159">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-160">Per ulteriori informazioni, vedere [bitmap e BitValues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d2501-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2501-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span><span class="sxs-lookup"><span data-stu-id="d2501-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-162">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2501-162">Data type: **string array**</span></span>

<span data-ttu-id="d2501-163">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-164">Conversione di un valore di posizione di bit in una **stringa** associata.</span><span class="sxs-lookup"><span data-stu-id="d2501-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="d2501-165">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-165">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-166">Per ulteriori informazioni, vedere [bitmap e BitValues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d2501-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2501-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Costruttore**</span><span class="sxs-lookup"><span data-stu-id="d2501-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-168">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-169">Si applica a: metodi</span><span class="sxs-lookup"><span data-stu-id="d2501-169">Applies to: methods</span></span>

<span data-ttu-id="d2501-170">Indica se il metodo crea istanze.</span><span class="sxs-lookup"><span data-stu-id="d2501-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="d2501-171">Questi metodi non sono limitati a agire su una sola istanza o su una singola classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="d2501-172">Un costruttore può, ad esempio, creare istanze di associazione, nonché istanze della classe che definiscono il costruttore.</span><span class="sxs-lookup"><span data-stu-id="d2501-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="d2501-173">Il qualificatore del **Costruttore** è destinato solo alle informazioni e non è previsto che venga utilizzato dal gestore di oggetti.</span><span class="sxs-lookup"><span data-stu-id="d2501-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="d2501-174">Il gestore di oggetti non deve chiamare i metodi del costruttore quando viene creato un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2501-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="d2501-175">Inoltre, quando viene chiamato un costruttore, il gestore di oggetti non deve richiamare alcun metodo del costruttore definito per una classe padre della classe originale.</span><span class="sxs-lookup"><span data-stu-id="d2501-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="d2501-176">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span><span class="sxs-lookup"><span data-stu-id="d2501-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-178">Data type: **string**</span></span>

<span data-ttu-id="d2501-179">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-179">Applies to: classes</span></span>

<span data-ttu-id="d2501-180">Nome del metodo in base al quale vengono create le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="d2501-181">Il valore è "PutInstance" o il nome di un altro metodo che crea le istanze.</span><span class="sxs-lookup"><span data-stu-id="d2501-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="d2501-182">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-182">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-183">Utilizzo: questo qualificatore può essere utilizzato solo se il qualificatore **SupportsCreate** è presente.</span><span class="sxs-lookup"><span data-stu-id="d2501-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span><span class="sxs-lookup"><span data-stu-id="d2501-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-185">Data type: **string**</span></span>

<span data-ttu-id="d2501-186">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-186">Applies to: classes</span></span>

<span data-ttu-id="d2501-187">Nome del metodo in base al quale vengono eliminate le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="d2501-188">Il valore può essere "DeleteInstance" o il nome di un altro metodo che elimina le istanze.</span><span class="sxs-lookup"><span data-stu-id="d2501-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="d2501-189">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-189">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-190">Utilizzo: questo qualificatore può essere utilizzato solo se il qualificatore **SupportsDelete** è presente.</span><span class="sxs-lookup"><span data-stu-id="d2501-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d2501-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-192">Data type: **string**</span></span>

<span data-ttu-id="d2501-193">Si applica a: any</span><span class="sxs-lookup"><span data-stu-id="d2501-193">Applies to: any</span></span>

<span data-ttu-id="d2501-194">Descrizione di un elemento denominato.</span><span class="sxs-lookup"><span data-stu-id="d2501-194">Description of a named element.</span></span> <span data-ttu-id="d2501-195">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Distruttore**</span><span class="sxs-lookup"><span data-stu-id="d2501-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-197">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-197">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-198">Si applica a: metodi</span><span class="sxs-lookup"><span data-stu-id="d2501-198">Applies to: methods</span></span>

<span data-ttu-id="d2501-199">Indica se il metodo elimina le istanze.</span><span class="sxs-lookup"><span data-stu-id="d2501-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="d2501-200">I metodi che usano il qualificatore del **distruttore** eliminano l'istanza o le istanze a cui viene applicato il distruttore e non sono vincolate a agire su una sola istanza o classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="d2501-201">Un distruttore, ad esempio, potrebbe eliminare le istanze dell'associazione, nonché le istanze della classe che definiscono il distruttore.</span><span class="sxs-lookup"><span data-stu-id="d2501-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="d2501-202">Il qualificatore del **distruttore** è destinato solo alle informazioni e non è previsto che venga utilizzato dal gestore di oggetti.</span><span class="sxs-lookup"><span data-stu-id="d2501-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="d2501-203">Non è necessario che il gestore di oggetti chiami un metodo con il qualificatore del **distruttore** quando un'istanza viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="d2501-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="d2501-204">Inoltre, quando viene chiamato un distruttore, il gestore di oggetti non deve richiamare alcun metodo di distruttore definito per una classe padre della classe originale.</span><span class="sxs-lookup"><span data-stu-id="d2501-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="d2501-205">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d2501-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-207">Data type: **string**</span></span>

<span data-ttu-id="d2501-208">Si applica a: any</span><span class="sxs-lookup"><span data-stu-id="d2501-208">Applies to: any</span></span>

<span data-ttu-id="d2501-209">Nome visualizzato nell'interfaccia utente anziché il nome effettivo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d2501-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="d2501-210">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span><span class="sxs-lookup"><span data-stu-id="d2501-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-212">Data type: **string**</span></span>

<span data-ttu-id="d2501-213">Si applica a: any</span><span class="sxs-lookup"><span data-stu-id="d2501-213">Applies to: any</span></span>

<span data-ttu-id="d2501-214">L'elemento di tipo stringa qualificato contiene un'istanza incorporata.</span><span class="sxs-lookup"><span data-stu-id="d2501-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="d2501-215">Il valore del qualificatore specifica il nome di una classe CIM nello stesso spazio dei nomi della classe che possiede l'elemento Qualified.</span><span class="sxs-lookup"><span data-stu-id="d2501-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="d2501-216">L'istanza incorporata è un'istanza della classe specificata, incluse le istanze delle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="d2501-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="d2501-217">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Calibro**</span><span class="sxs-lookup"><span data-stu-id="d2501-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-219">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-220">Si applica a: any</span><span class="sxs-lookup"><span data-stu-id="d2501-220">Applies to: any</span></span>

<span data-ttu-id="d2501-221">Indica se la proprietà rappresenta un numero intero non negativo, che può aumentare o diminuire, ma mai superare un valore massimo.</span><span class="sxs-lookup"><span data-stu-id="d2501-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="d2501-222">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-222">The default is **FALSE**.</span></span>

<span data-ttu-id="d2501-223">Il valore massimo della proprietà non può essere maggiore di 2 ^*n* -1.</span><span class="sxs-lookup"><span data-stu-id="d2501-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="d2501-224">*N* può essere 8, 16, 32 o 64 a seconda del tipo di dati della proprietà a cui viene applicato questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d2501-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="d2501-225">Il valore di un misuratore ha il valore massimo ogni volta che le informazioni modellate sono maggiori o uguali al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="d2501-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="d2501-226">Se le informazioni modellate successivamente diminuiscono al di sotto del valore massimo, il misuratore diminuisce anche.</span><span class="sxs-lookup"><span data-stu-id="d2501-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="d2501-227">Questo qualificatore è applicabile solo alle proprietà con tipo di dati Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="d2501-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span><span class="sxs-lookup"><span data-stu-id="d2501-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-229">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-229">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-230">Si applica a: parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-230">Applies to: parameters</span></span>

<span data-ttu-id="d2501-231">Indica se il parametro viene utilizzato per passare valori a un metodo.</span><span class="sxs-lookup"><span data-stu-id="d2501-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="d2501-232">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d2501-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In uscita**</span><span class="sxs-lookup"><span data-stu-id="d2501-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-234">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-234">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-235">Si applica a: parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-235">Applies to: parameters</span></span>

<span data-ttu-id="d2501-236">Indica se il parametro è un parametro di input e di output.</span><span class="sxs-lookup"><span data-stu-id="d2501-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Chiave**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d2501-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d2501-238">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-238">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-239">Si applica a: proprietà, riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-239">Applies to: properties, references</span></span>

<span data-ttu-id="d2501-240">Indica se la proprietà fa parte dell'handle dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d2501-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="d2501-241">Se più di una proprietà dispone del qualificatore [**chiave**](key-qualifier.md) , tutte queste proprietà costituiscono collettivamente la chiave (una chiave composta).</span><span class="sxs-lookup"><span data-stu-id="d2501-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="d2501-242">Quando vengono rilevate insieme, le proprietà chiave devono fornire un riferimento univoco per ogni istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="d2501-243">Se questo qualificatore viene inserito in una proprietà, è consentito solo il valore **true** .</span><span class="sxs-lookup"><span data-stu-id="d2501-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span><span class="sxs-lookup"><span data-stu-id="d2501-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-245">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-245">Applies to: properties</span></span>

<span data-ttu-id="d2501-246">Indica che la proprietà è a elevato utilizzo di risorse e richiede molto tempo e memoria del processore.</span><span class="sxs-lookup"><span data-stu-id="d2501-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="d2501-247">WMI migliora le prestazioni delle query non tentando di restituire le proprietà contrassegnate dal qualificatore **Lazy** .</span><span class="sxs-lookup"><span data-stu-id="d2501-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span><span class="sxs-lookup"><span data-stu-id="d2501-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-249">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2501-249">Data type: **string array**</span></span>

<span data-ttu-id="d2501-250">Si applica a: classi, proprietà, associazioni, indicazioni, riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="d2501-251">Set di valori che indicano il percorso di una posizione in cui è possibile trovare ulteriori informazioni sull'origine di una proprietà, una classe, un'associazione, un'indicazione o un riferimento.</span><span class="sxs-lookup"><span data-stu-id="d2501-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="d2501-252">La stringa di mapping può essere un percorso di directory, un URL, una chiave del registro di sistema, un file di inclusione, un riferimento a una classe CIM o un altro formato.</span><span class="sxs-lookup"><span data-stu-id="d2501-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="d2501-253">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span><span class="sxs-lookup"><span data-stu-id="d2501-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-255">Tipo di dati: **int**</span><span class="sxs-lookup"><span data-stu-id="d2501-255">Data type: **int**</span></span>

<span data-ttu-id="d2501-256">Si applica a: riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-256">Applies to: references</span></span>

<span data-ttu-id="d2501-257">Numero massimo di valori che possono essere presenti in un determinato riferimento per ogni set di altri valori di riferimento nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="d2501-258">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-258">The default is **NULL**.</span></span> <span data-ttu-id="d2501-259">Se, ad esempio, un'associazione mette in correlazione un'istanza alle istanze di B e deve essere presente al massimo un'istanza per ogni istanza B, il riferimento a un oggetto deve avere un massimo di un qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d2501-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="d2501-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-261">Tipo di dati: **int**</span><span class="sxs-lookup"><span data-stu-id="d2501-261">Data type: **int**</span></span>

<span data-ttu-id="d2501-262">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-263">Lunghezza massima (in caratteri) di un elemento di dati **stringa** e indica il supporto di matrici a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="d2501-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="d2501-264">Se viene rilevata una matrice a lunghezza fissa, il qualificatore **maxlen** contiene la lunghezza fissa trovata durante l'analisi.</span><span class="sxs-lookup"><span data-stu-id="d2501-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="d2501-265">Se viene rilevata una matrice a lunghezza variabile, questo qualificatore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d2501-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="d2501-266">**Maxlen** viene usato per suggerire il numero massimo di elementi che devono essere archiviati in una matrice.</span><span class="sxs-lookup"><span data-stu-id="d2501-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="d2501-267">Quando si esegue l'override del valore predefinito, è possibile specificare qualsiasi valore di Unsigned Integer (**UInt32**).</span><span class="sxs-lookup"><span data-stu-id="d2501-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="d2501-268">Il valore **null** (impostazione predefinita) implica una lunghezza illimitata.</span><span class="sxs-lookup"><span data-stu-id="d2501-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="d2501-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-270">Tipo di dati: **int**</span><span class="sxs-lookup"><span data-stu-id="d2501-270">Data type: **int**</span></span>

<span data-ttu-id="d2501-271">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-272">Valore massimo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2501-272">Maximum value of the object.</span></span> <span data-ttu-id="d2501-273">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span><span class="sxs-lookup"><span data-stu-id="d2501-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-275">Tipo di dati: **int**</span><span class="sxs-lookup"><span data-stu-id="d2501-275">Data type: **int**</span></span>

<span data-ttu-id="d2501-276">Si applica a: riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-276">Applies to: references</span></span>

<span data-ttu-id="d2501-277">Cardinalità minima del riferimento (il numero minimo di valori che un determinato riferimento può avere per ogni set di altri valori di riferimento nell'associazione).</span><span class="sxs-lookup"><span data-stu-id="d2501-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="d2501-278">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="d2501-278">The default is 0.</span></span>

<span data-ttu-id="d2501-279">Se, ad esempio, un'associazione mette in relazione le istanze di in istanze B e deve essere presente almeno un'istanza per ogni istanza B, il riferimento a un oggetto deve avere almeno un qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d2501-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="d2501-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-281">Tipo di dati: **int**</span><span class="sxs-lookup"><span data-stu-id="d2501-281">Data type: **int**</span></span>

<span data-ttu-id="d2501-282">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-283">Indica il valore minimo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2501-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="d2501-284">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span><span class="sxs-lookup"><span data-stu-id="d2501-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-286">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2501-286">Data type: **string array**</span></span>

<span data-ttu-id="d2501-287">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-287">Applies to: properties</span></span>

<span data-ttu-id="d2501-288">Set di valori che indicano la corrispondenza tra la proprietà di un oggetto e altre proprietà nello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="d2501-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="d2501-289">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-289">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-290">Le proprietà dell'oggetto vengono identificate utilizzando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="d2501-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="d2501-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="d2501-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="d2501-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Non locali**</span><span class="sxs-lookup"><span data-stu-id="d2501-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-293">Data type: **string**</span></span>

<span data-ttu-id="d2501-294">Si applica a: riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-294">Applies to: references</span></span>

<span data-ttu-id="d2501-295">Percorso di un'istanza, il cui valore è <*tipologia*>://<*namespacehandle*> il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="d2501-296">Utilizzo: questo qualificatore non può essere utilizzato con il qualificatore **NonlocalType** .</span><span class="sxs-lookup"><span data-stu-id="d2501-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span><span class="sxs-lookup"><span data-stu-id="d2501-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-298">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-298">Data type: **string**</span></span>

<span data-ttu-id="d2501-299">Si applica a: riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-299">Applies to: references</span></span>

<span data-ttu-id="d2501-300">Tipo di posizione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="d2501-300">Type of location of an instance.</span></span> <span data-ttu-id="d2501-301">Il valore è <namespacetype> .</span><span class="sxs-lookup"><span data-stu-id="d2501-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="d2501-302">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-302">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-303">Utilizzo: questo qualificatore non può essere utilizzato con il qualificatore non **locale** .</span><span class="sxs-lookup"><span data-stu-id="d2501-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="d2501-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-305">Data type: **string**</span></span>

<span data-ttu-id="d2501-306">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-306">Applies to: properties</span></span>

<span data-ttu-id="d2501-307">Valore che indica che la proprietà associata è **null** (la proprietà non ha un valore valido o significativo).</span><span class="sxs-lookup"><span data-stu-id="d2501-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="d2501-308">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-308">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-309">Le convenzioni e le restrizioni usate per la definizione dei valori **null** sono le stesse applicabili al qualificatore **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="d2501-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="d2501-310">Nota non è possibile eseguire l'override di questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="d2501-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="d2501-311">Non è ragionevole consentire a una sottoclasse di restituire un valore **null** diverso rispetto a quello della classe padre.</span><span class="sxs-lookup"><span data-stu-id="d2501-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span><span class="sxs-lookup"><span data-stu-id="d2501-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-313">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-313">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-314">Si applica a: parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-314">Applies to: parameters</span></span>

<span data-ttu-id="d2501-315">Indica se il parametro restituisce valori da un metodo.</span><span class="sxs-lookup"><span data-stu-id="d2501-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="d2501-316">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span><span class="sxs-lookup"><span data-stu-id="d2501-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-318">Data type: **string**</span></span>

<span data-ttu-id="d2501-319">Si applica a: proprietà, metodi, riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="d2501-320">Classe padre o costrutto subordinato (proprietà, metodo o riferimento) sottoposto a override dalla proprietà, dal metodo o dal riferimento con lo stesso nome nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="d2501-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="d2501-321">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-321">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-322">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="d2501-322">The format is:</span></span>

<span data-ttu-id="d2501-323">\[<> della *classe* . \] < *costrutto subordinato*></span><span class="sxs-lookup"><span data-stu-id="d2501-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="d2501-324">Se il nome della classe viene omesso, l'override viene applicato al costrutto subordinato nella classe padre nella gerarchia di classi.</span><span class="sxs-lookup"><span data-stu-id="d2501-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="d2501-325">Utilizzo: il qualificatore di **override** può fare riferimento a costrutti basati solo sullo stesso Metamodello.</span><span class="sxs-lookup"><span data-stu-id="d2501-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="d2501-326">Non è consentito modificare il nome o la firma di un costrutto durante un'operazione di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="d2501-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span><span class="sxs-lookup"><span data-stu-id="d2501-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-328">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-328">Applies to: classes</span></span>

<span data-ttu-id="d2501-329">Indica se il valore della proprietà in una sottoclasse esegue l'override del valore in una classe padre.</span><span class="sxs-lookup"><span data-stu-id="d2501-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="d2501-330">L'implicazione funzionale è che, se si esegue una query sulla classe padre e se la clausola **where** include questa proprietà, l'elemento padre deve restituire un'istanza con il valore sottoposto a override.</span><span class="sxs-lookup"><span data-stu-id="d2501-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="d2501-331">Di conseguenza, gestione Windows regola la clausola **where** della query inviata alla classe padre per escludere i riferimenti a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2501-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagate**</span><span class="sxs-lookup"><span data-stu-id="d2501-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-333">Data type: **string**</span></span>

<span data-ttu-id="d2501-334">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-334">Applies to: properties</span></span>

<span data-ttu-id="d2501-335">Nome della chiave da propagare.</span><span class="sxs-lookup"><span data-stu-id="d2501-335">Name of the key being propagated.</span></span> <span data-ttu-id="d2501-336">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-336">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-337">L'uso di questo qualificatore presuppone l'esistenza di un solo qualificatore vulnerabile su un riferimento che abbia la classe che lo contiene come destinazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="d2501-338">La proprietà associata deve avere lo stesso valore della proprietà indicata dal qualificatore nella classe sull'altro lato dell'associazione debole.</span><span class="sxs-lookup"><span data-stu-id="d2501-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="d2501-339">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="d2501-339">The format is:</span></span>

<span data-ttu-id="d2501-340">\[<> della *classe* . \] < *costrutto subordinato*></span><span class="sxs-lookup"><span data-stu-id="d2501-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="d2501-341">Utilizzo: quando viene usato il qualificatore **propagato** , il qualificatore della [**chiave**](key-qualifier.md) deve essere specificato con un valore **true**.</span><span class="sxs-lookup"><span data-stu-id="d2501-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Lettura**</span><span class="sxs-lookup"><span data-stu-id="d2501-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-343">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-343">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-344">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-344">Applies to: properties</span></span>

<span data-ttu-id="d2501-345">Indica se la proprietà è leggibile.</span><span class="sxs-lookup"><span data-stu-id="d2501-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="d2501-346">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d2501-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="d2501-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-348">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-348">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-349">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-349">Applies to: properties</span></span>

<span data-ttu-id="d2501-350">Indica se per la proprietà è necessario un valore non null.</span><span class="sxs-lookup"><span data-stu-id="d2501-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="d2501-351">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisione**</span><span class="sxs-lookup"><span data-stu-id="d2501-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-353">Data type: **string**</span></span>

<span data-ttu-id="d2501-354">Si applica a: classi, associazioni, indicazioni, schemi</span><span class="sxs-lookup"><span data-stu-id="d2501-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="d2501-355">Numero di revisione secondario dell'oggetto dello schema.</span><span class="sxs-lookup"><span data-stu-id="d2501-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="d2501-356">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-356">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-357">Usage: il qualificatore di **versione** deve essere presente per fornire il numero di versione principale quando viene usato il qualificatore di **Revisione** .</span><span class="sxs-lookup"><span data-stu-id="d2501-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span><span class="sxs-lookup"><span data-stu-id="d2501-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-359">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-359">Data type: **string**</span></span>

<span data-ttu-id="d2501-360">Si applica a: proprietà, metodi</span><span class="sxs-lookup"><span data-stu-id="d2501-360">Applies to: properties, methods</span></span>

<span data-ttu-id="d2501-361">Nome dello schema in cui è definita la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d2501-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="d2501-362">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Origine**</span><span class="sxs-lookup"><span data-stu-id="d2501-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-364">Data type: **string**</span></span>

<span data-ttu-id="d2501-365">Si applica a: classi, associazioni, indicazioni, riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="d2501-366">Percorso di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="d2501-366">Location of an instance.</span></span> <span data-ttu-id="d2501-367">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-367">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-368">Il valore del qualificatore è <*tipologia*>://<*namespacehandle*>.</span><span class="sxs-lookup"><span data-stu-id="d2501-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="d2501-369">Uso: il qualificatore di **origine** non può essere usato con il qualificatore **sourceType** .</span><span class="sxs-lookup"><span data-stu-id="d2501-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span><span class="sxs-lookup"><span data-stu-id="d2501-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-371">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-371">Data type: **string**</span></span>

<span data-ttu-id="d2501-372">Si applica a: classi, associazioni, indicazioni, riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="d2501-373">Tipo di posizione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="d2501-373">Type of location of an instance.</span></span> <span data-ttu-id="d2501-374">Il valore di questo qualificatore è <> *tipologia* .</span><span class="sxs-lookup"><span data-stu-id="d2501-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="d2501-375">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-375">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-376">Utilizzo: non è possibile utilizzare il qualificatore **sourceType** con il qualificatore di **origine** .</span><span class="sxs-lookup"><span data-stu-id="d2501-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span><span class="sxs-lookup"><span data-stu-id="d2501-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-378">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-378">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-379">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-379">Applies to: classes</span></span>

<span data-ttu-id="d2501-380">Indica se la classe supporta la creazione di istanze.</span><span class="sxs-lookup"><span data-stu-id="d2501-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="d2501-381">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="d2501-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-383">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-383">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-384">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-384">Applies to: classes</span></span>

<span data-ttu-id="d2501-385">Indica se la classe supporta l'eliminazione di istanze di.</span><span class="sxs-lookup"><span data-stu-id="d2501-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="d2501-386">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span><span class="sxs-lookup"><span data-stu-id="d2501-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-388">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-388">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-389">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-389">Applies to: classes</span></span>

<span data-ttu-id="d2501-390">Indica se la classe supporta la modifica (aggiornamento) delle istanze di.</span><span class="sxs-lookup"><span data-stu-id="d2501-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="d2501-391">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span><span class="sxs-lookup"><span data-stu-id="d2501-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-393">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-393">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-394">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="d2501-394">Applies to: classes</span></span>

<span data-ttu-id="d2501-395">Indica se la classe può disporre di sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="d2501-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="d2501-396">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-396">The default is **FALSE**.</span></span>

<span data-ttu-id="d2501-397">Se viene dichiarata una sottoclasse, il compilatore genera un errore.</span><span class="sxs-lookup"><span data-stu-id="d2501-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="d2501-398">Utilizzo: questo qualificatore non può coesistere con il qualificatore **astratto** .</span><span class="sxs-lookup"><span data-stu-id="d2501-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="d2501-399">Se vengono specificati entrambi i qualificatori **Terminal** e **abstract** , il compilatore genera un errore.</span><span class="sxs-lookup"><span data-stu-id="d2501-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Unità**</span><span class="sxs-lookup"><span data-stu-id="d2501-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-401">Data type: **string**</span></span>

<span data-ttu-id="d2501-402">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-403">Tipo di unità in cui viene espresso l'elemento di dati associato.</span><span class="sxs-lookup"><span data-stu-id="d2501-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="d2501-404">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-404">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-405">Ad esempio, un elemento di dati di dimensioni potrebbe avere un valore di "bytes" per le **unità**.</span><span class="sxs-lookup"><span data-stu-id="d2501-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="d2501-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-407">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2501-407">Data type: **string array**</span></span>

<span data-ttu-id="d2501-408">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-409">Set di valori consentiti per una proprietà, un tipo restituito del metodo o un parametro del metodo.</span><span class="sxs-lookup"><span data-stu-id="d2501-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="d2501-410">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-410">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-411">Usage: questo qualificatore può essere usato da solo o in combinazione con il qualificatore **values** .</span><span class="sxs-lookup"><span data-stu-id="d2501-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="d2501-412">Se usato in combinazione con il qualificatore **values** , il percorso del valore nella matrice **ValueMap** fornisce la posizione della voce corrispondente nella matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="d2501-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="d2501-413">Usare il qualificatore **ValueMap** solo con valori stringa e interi.</span><span class="sxs-lookup"><span data-stu-id="d2501-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="d2501-414">La sintassi per la rappresentazione di un valore integer nella matrice della mappa dei valori è digit \[ + \| = \] \[ \* digit \] .</span><span class="sxs-lookup"><span data-stu-id="d2501-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="d2501-415">Il contenuto, il numero massimo di cifre e il valore rappresentato sono limitati dal tipo della proprietà associata.</span><span class="sxs-lookup"><span data-stu-id="d2501-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="d2501-416">Ad esempio, Uint8 non può essere firmato, deve essere composto da meno di quattro cifre e deve rappresentare un valore inferiore a 256.</span><span class="sxs-lookup"><span data-stu-id="d2501-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valori**</span><span class="sxs-lookup"><span data-stu-id="d2501-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-418">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="d2501-418">Data type: **string array**</span></span>

<span data-ttu-id="d2501-419">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="d2501-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d2501-420">Set di valori che converte un valore integer in una stringa associata.</span><span class="sxs-lookup"><span data-stu-id="d2501-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="d2501-421">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-421">The default is **NULL**.</span></span>

<span data-ttu-id="d2501-422">Questa proprietà specifica inoltre una matrice di valori stringa di cui eseguire il mapping a una proprietà di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="d2501-423">Questo qualificatore può essere applicato a una proprietà Integer o a una proprietà di stringa e il mapping può essere implicito o esplicito.</span><span class="sxs-lookup"><span data-stu-id="d2501-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="d2501-424">Se il mapping è implicito, i valori di proprietà Integer o String rappresentano posizioni ordinali nella matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="d2501-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="d2501-425">Se il mapping è esplicito, la proprietà deve essere un numero intero e i valori di proprietà validi sono elencati nella matrice definita dal qualificatore **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="d2501-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="d2501-426">Per ulteriori informazioni, vedere [mapping dei valori](value-map.md).</span><span class="sxs-lookup"><span data-stu-id="d2501-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="d2501-427">Se non è presente un qualificatore **ValueMap** , la matrice di **valori** viene indicizzata (relativa a zero) utilizzando il valore nella proprietà associata, nel tipo restituito del metodo o nel parametro del metodo.</span><span class="sxs-lookup"><span data-stu-id="d2501-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="d2501-428">Se è presente un qualificatore **ValueMap** , l'indice dei valori viene definito in base alla posizione del valore della proprietà nella mappa del valore.</span><span class="sxs-lookup"><span data-stu-id="d2501-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione**</span><span class="sxs-lookup"><span data-stu-id="d2501-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d2501-430">Data type: **string**</span></span>

<span data-ttu-id="d2501-431">Si applica a: classi, schemi, associazioni, indicazioni</span><span class="sxs-lookup"><span data-stu-id="d2501-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="d2501-432">Numero di versione principale dell'oggetto dello schema.</span><span class="sxs-lookup"><span data-stu-id="d2501-432">Major version number of the schema object.</span></span> <span data-ttu-id="d2501-433">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="d2501-433">The default is **NULL**.</span></span> <span data-ttu-id="d2501-434">Il numero di versione viene incrementato quando vengono apportate modifiche allo schema che modificano l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d2501-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Debole**</span><span class="sxs-lookup"><span data-stu-id="d2501-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-436">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-436">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-437">Si applica a: riferimenti</span><span class="sxs-lookup"><span data-stu-id="d2501-437">Applies to: references</span></span>

<span data-ttu-id="d2501-438">Indica se le chiavi della classe a cui si fa riferimento includono le chiavi degli altri partecipanti nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="d2501-439">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-439">The default is **FALSE**.</span></span>

<span data-ttu-id="d2501-440">Questo qualificatore viene utilizzato quando l'identità della classe a cui si fa riferimento dipende dall'identità degli altri partecipanti nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d2501-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="d2501-441">Non più di un riferimento a una determinata classe può essere vulnerabile.</span><span class="sxs-lookup"><span data-stu-id="d2501-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="d2501-442">Le altre classi nell'associazione devono definire una chiave.</span><span class="sxs-lookup"><span data-stu-id="d2501-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="d2501-443">Le chiavi delle altre classi nell'associazione vengono ripetute nella classe a cui si fa riferimento e sono contrassegnate con un qualificatore **propagato** .</span><span class="sxs-lookup"><span data-stu-id="d2501-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Scrittura**</span><span class="sxs-lookup"><span data-stu-id="d2501-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-445">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-445">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-446">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-446">Applies to: properties</span></span>

<span data-ttu-id="d2501-447">Indica che le applicazioni o gli script possono modificare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2501-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="d2501-448">L'account che esegue l'applicazione deve avere accesso allo spazio dei nomi che contiene le istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="d2501-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="d2501-449">L'implementazione del provider può anche limitare l'accesso ai dati del provider.</span><span class="sxs-lookup"><span data-stu-id="d2501-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="d2501-450">Il valore **true** indica che la proprietà è leggibile e scrivibile dai consumer a cui è consentito l'accesso da parte di WMI e del provider.</span><span class="sxs-lookup"><span data-stu-id="d2501-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="d2501-451">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-451">The default is **FALSE**.</span></span>

<span data-ttu-id="d2501-452">Una proprietà che non dispone del qualificatore di **scrittura** può comunque essere scrivibile.</span><span class="sxs-lookup"><span data-stu-id="d2501-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="d2501-453">L'implementazione del provider può consentire la modifica di qualsiasi proprietà nelle classi del provider, indipendentemente dal fatto che sia presente il qualificatore di **scrittura** .</span><span class="sxs-lookup"><span data-stu-id="d2501-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span><span class="sxs-lookup"><span data-stu-id="d2501-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-455">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-455">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-456">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-456">Applies to: properties</span></span>

<span data-ttu-id="d2501-457">Indica se la proprietà è scrivibile durante la creazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d2501-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="d2501-458">Questo qualificatore può essere utilizzato insieme al qualificatore **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="d2501-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="d2501-459">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2501-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span><span class="sxs-lookup"><span data-stu-id="d2501-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="d2501-461">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d2501-461">Data type: **boolean**</span></span>

<span data-ttu-id="d2501-462">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2501-462">Applies to: properties</span></span>

<span data-ttu-id="d2501-463">Indica se la proprietà è scrivibile in caso di aggiornamento dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d2501-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="d2501-464">Questo qualificatore può essere utilizzato insieme al qualificatore **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="d2501-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="d2501-465">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="d2501-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d2501-466">Esempio</span><span class="sxs-lookup"><span data-stu-id="d2501-466">Examples</span></span>

<span data-ttu-id="d2501-467">Per ulteriori informazioni sul recupero dei qualificatori, vedere l'esempio di codice PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) nella raccolta TechNet.</span><span class="sxs-lookup"><span data-stu-id="d2501-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2501-468">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2501-468">Requirements</span></span>



| <span data-ttu-id="d2501-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2501-469">Requirement</span></span> | <span data-ttu-id="d2501-470">Valore</span><span class="sxs-lookup"><span data-stu-id="d2501-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d2501-471">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2501-471">Minimum supported client</span></span><br/> | <span data-ttu-id="d2501-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2501-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d2501-473">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2501-473">Minimum supported server</span></span><br/> | <span data-ttu-id="d2501-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2501-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2501-475">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2501-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2501-476">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="d2501-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="d2501-477">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="d2501-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




