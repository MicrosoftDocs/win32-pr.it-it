---
description: La tabella ModuleConfiguration identifica gli attributi configurabili del modulo. Questa tabella non è unita nel database.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Tabella ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232070"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="1095e-104">Tabella ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1095e-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="1095e-105">La tabella ModuleConfiguration identifica gli attributi configurabili del modulo.</span><span class="sxs-lookup"><span data-stu-id="1095e-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="1095e-106">Questa tabella non è unita nel database.</span><span class="sxs-lookup"><span data-stu-id="1095e-106">This table is not merged into the database.</span></span>

<span data-ttu-id="1095e-107">La tabella ModuleConfiguration include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="1095e-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="1095e-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="1095e-108">Column</span></span>       | <span data-ttu-id="1095e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1095e-109">Type</span></span>                         | <span data-ttu-id="1095e-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="1095e-110">Key</span></span> | <span data-ttu-id="1095e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="1095e-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="1095e-112">Nome</span><span class="sxs-lookup"><span data-stu-id="1095e-112">Name</span></span>         | [<span data-ttu-id="1095e-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="1095e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="1095e-114">S</span><span class="sxs-lookup"><span data-stu-id="1095e-114">Y</span></span>   | <span data-ttu-id="1095e-115">N</span><span class="sxs-lookup"><span data-stu-id="1095e-115">N</span></span>        |
| <span data-ttu-id="1095e-116">Formato</span><span class="sxs-lookup"><span data-stu-id="1095e-116">Format</span></span>       | [<span data-ttu-id="1095e-117">Integer</span><span class="sxs-lookup"><span data-stu-id="1095e-117">Integer</span></span>](integer.md)       | <span data-ttu-id="1095e-118">N</span><span class="sxs-lookup"><span data-stu-id="1095e-118">N</span></span>   | <span data-ttu-id="1095e-119">N</span><span class="sxs-lookup"><span data-stu-id="1095e-119">N</span></span>        |
| <span data-ttu-id="1095e-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="1095e-120">Type</span></span>         | [<span data-ttu-id="1095e-121">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-121">Text</span></span>](text.md)             | <span data-ttu-id="1095e-122">N</span><span class="sxs-lookup"><span data-stu-id="1095e-122">N</span></span>   | <span data-ttu-id="1095e-123">S</span><span class="sxs-lookup"><span data-stu-id="1095e-123">Y</span></span>        |
| <span data-ttu-id="1095e-124">ContextData</span><span class="sxs-lookup"><span data-stu-id="1095e-124">ContextData</span></span>  | [<span data-ttu-id="1095e-125">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-125">Text</span></span>](text.md)             | <span data-ttu-id="1095e-126">N</span><span class="sxs-lookup"><span data-stu-id="1095e-126">N</span></span>   | <span data-ttu-id="1095e-127">S</span><span class="sxs-lookup"><span data-stu-id="1095e-127">Y</span></span>        |
| <span data-ttu-id="1095e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1095e-128">DefaultValue</span></span> | [<span data-ttu-id="1095e-129">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-129">Text</span></span>](text.md)             | <span data-ttu-id="1095e-130">N</span><span class="sxs-lookup"><span data-stu-id="1095e-130">N</span></span>   | <span data-ttu-id="1095e-131">S</span><span class="sxs-lookup"><span data-stu-id="1095e-131">Y</span></span>        |
| <span data-ttu-id="1095e-132">Attributi</span><span class="sxs-lookup"><span data-stu-id="1095e-132">Attributes</span></span>   | [<span data-ttu-id="1095e-133">Integer</span><span class="sxs-lookup"><span data-stu-id="1095e-133">Integer</span></span>](integer.md)       | <span data-ttu-id="1095e-134">N</span><span class="sxs-lookup"><span data-stu-id="1095e-134">N</span></span>   | <span data-ttu-id="1095e-135">S</span><span class="sxs-lookup"><span data-stu-id="1095e-135">Y</span></span>        |
| <span data-ttu-id="1095e-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="1095e-136">DisplayName</span></span>  | [<span data-ttu-id="1095e-137">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-137">Text</span></span>](text.md)             | <span data-ttu-id="1095e-138">N</span><span class="sxs-lookup"><span data-stu-id="1095e-138">N</span></span>   | <span data-ttu-id="1095e-139">S</span><span class="sxs-lookup"><span data-stu-id="1095e-139">Y</span></span>        |
| <span data-ttu-id="1095e-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1095e-140">Description</span></span>  | [<span data-ttu-id="1095e-141">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-141">Text</span></span>](text.md)             | <span data-ttu-id="1095e-142">N</span><span class="sxs-lookup"><span data-stu-id="1095e-142">N</span></span>   | <span data-ttu-id="1095e-143">S</span><span class="sxs-lookup"><span data-stu-id="1095e-143">Y</span></span>        |
| <span data-ttu-id="1095e-144">HelpLocation</span><span class="sxs-lookup"><span data-stu-id="1095e-144">HelpLocation</span></span> | [<span data-ttu-id="1095e-145">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-145">Text</span></span>](text.md)             | <span data-ttu-id="1095e-146">N</span><span class="sxs-lookup"><span data-stu-id="1095e-146">N</span></span>   | <span data-ttu-id="1095e-147">S</span><span class="sxs-lookup"><span data-stu-id="1095e-147">Y</span></span>        |
| <span data-ttu-id="1095e-148">HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="1095e-148">HelpKeyword</span></span>  | [<span data-ttu-id="1095e-149">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-149">Text</span></span>](text.md)             | <span data-ttu-id="1095e-150">N</span><span class="sxs-lookup"><span data-stu-id="1095e-150">N</span></span>   | <span data-ttu-id="1095e-151">S</span><span class="sxs-lookup"><span data-stu-id="1095e-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1095e-152">Colonne</span><span class="sxs-lookup"><span data-stu-id="1095e-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1095e-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="1095e-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="1095e-154">Questo campo definisce il nome dell'elemento configurabile.</span><span class="sxs-lookup"><span data-stu-id="1095e-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="1095e-155">A questo nome viene fatto riferimento nel modello di formattazione della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="1095e-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1095e-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Formato</span><span class="sxs-lookup"><span data-stu-id="1095e-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="1095e-157">Questa colonna specifica il formato dei dati da modificare.</span><span class="sxs-lookup"><span data-stu-id="1095e-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="1095e-158">Formato</span><span class="sxs-lookup"><span data-stu-id="1095e-158">Format</span></span>                                       | <span data-ttu-id="1095e-159">Valore</span><span class="sxs-lookup"><span data-stu-id="1095e-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="1095e-160">Text</span><span class="sxs-lookup"><span data-stu-id="1095e-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="1095e-161">0</span><span class="sxs-lookup"><span data-stu-id="1095e-161">0</span></span>     |
| [<span data-ttu-id="1095e-162">Chiave</span><span class="sxs-lookup"><span data-stu-id="1095e-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="1095e-163">1</span><span class="sxs-lookup"><span data-stu-id="1095e-163">1</span></span>     |
| [<span data-ttu-id="1095e-164">Integer</span><span class="sxs-lookup"><span data-stu-id="1095e-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="1095e-165">2</span><span class="sxs-lookup"><span data-stu-id="1095e-165">2</span></span>     |
| [<span data-ttu-id="1095e-166">Formato bit</span><span class="sxs-lookup"><span data-stu-id="1095e-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="1095e-167">3</span><span class="sxs-lookup"><span data-stu-id="1095e-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="1095e-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo</span><span class="sxs-lookup"><span data-stu-id="1095e-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="1095e-169">In questa colonna viene specificato il tipo per i dati da modificare.</span><span class="sxs-lookup"><span data-stu-id="1095e-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="1095e-170">Questo tipo viene utilizzato per fornire un contesto per qualsiasi interfaccia utente e non viene utilizzato nel processo di merge.</span><span class="sxs-lookup"><span data-stu-id="1095e-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="1095e-171">I valori validi per questa colonna dipendono dal valore nella colonna formato.</span><span class="sxs-lookup"><span data-stu-id="1095e-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="1095e-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span><span class="sxs-lookup"><span data-stu-id="1095e-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="1095e-173">Questa colonna specifica un contesto semantico per i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="1095e-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="1095e-174">Il tipo viene utilizzato per fornire un contesto per qualsiasi interfaccia utente e non viene utilizzato nel processo di merge.</span><span class="sxs-lookup"><span data-stu-id="1095e-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="1095e-175">I valori validi per questa colonna dipendono dai valori nelle colonne format e Type.</span><span class="sxs-lookup"><span data-stu-id="1095e-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="1095e-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1095e-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="1095e-177">In questa colonna viene specificato un valore predefinito per l'elemento in questo record se lo strumento di merge rifiuta di fornire un valore.</span><span class="sxs-lookup"><span data-stu-id="1095e-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="1095e-178">Questo valore deve avere il formato, il tipo e il contesto dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1095e-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="1095e-179">Se si tratta di un elemento di formato "chiave", la chiave esterna deve essere una chiave valida nelle tabelle del modulo.</span><span class="sxs-lookup"><span data-stu-id="1095e-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="1095e-180">Null può essere un valore valido per questa colonna a seconda dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1095e-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="1095e-181">Per gli elementi di formato "Key", questo valore è in [formato speciale CMSM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="1095e-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="1095e-182">Per tutti gli altri tipi, il valore viene trattato letteralmente.</span><span class="sxs-lookup"><span data-stu-id="1095e-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="1095e-183">Gli autori dei moduli devono assicurarsi che il modulo sia valido nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="1095e-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="1095e-184">Ciò garantisce che le versioni di Mergemod.dll precedenti alla versione 2,0 possano ancora usare il modulo nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="1095e-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="1095e-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="1095e-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="1095e-186">Questa colonna è un campo di bit contenente gli attributi per questo elemento configurabile.</span><span class="sxs-lookup"><span data-stu-id="1095e-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="1095e-187">Null equivale a 0.</span><span class="sxs-lookup"><span data-stu-id="1095e-187">Null is equivalent to 0.</span></span> <span data-ttu-id="1095e-188">Tutti gli altri bit in questa colonna sono riservati per utilizzi futuri e devono essere pari a 0.</span><span class="sxs-lookup"><span data-stu-id="1095e-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="1095e-189">Nome</span><span class="sxs-lookup"><span data-stu-id="1095e-189">Name</span></span>                             | <span data-ttu-id="1095e-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="1095e-190">Decimal</span></span> | <span data-ttu-id="1095e-191">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="1095e-191">Hexadecimal</span></span> | <span data-ttu-id="1095e-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1095e-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1095e-193">msmConfigurableOptionKeyNoOrphan</span><span class="sxs-lookup"><span data-stu-id="1095e-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="1095e-194">1</span><span class="sxs-lookup"><span data-stu-id="1095e-194">1</span></span>       | <span data-ttu-id="1095e-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1095e-195">0x00000001</span></span>  | <span data-ttu-id="1095e-196">Questo attributo si applica solo ai record che elencano una chiave esterna di una tabella del modulo nel campo DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="1095e-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="1095e-197">Lo strumento Merge ignora l'attributo per tutti i formati diversi dai [tipi di formato chiave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="1095e-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="1095e-198">Gli elementi non elencati nella [tabella ModuleSubstitution](modulesubstitution-table.md) sono esclusi dal controllo seguente.</span><span class="sxs-lookup"><span data-stu-id="1095e-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="1095e-199">Lo strumento merge non unisce la riga a cui fa riferimento la colonna DefaultValue nel database di destinazione se vengono soddisfatte le condizioni seguenti dopo aver completato tutte le opzioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1095e-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="1095e-200">Ogni riga della tabella ModuleConfiguration con lo stesso DefaultValue dispone del set di msmConfigurationItemsKeyNoOrphan.</span><span class="sxs-lookup"><span data-stu-id="1095e-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="1095e-201">Nessuna riga USA DefaultValue perché lo strumento di creazione ha rifiutato di fornire un valore.</span><span class="sxs-lookup"><span data-stu-id="1095e-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="1095e-202">Lo strumento di merge unisce la riga se viene soddisfatta una delle condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1095e-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="1095e-203">Lo strumento Merge trova una riga in cui non è impostato msmConfigItemsKeyNoOrphan.</span><span class="sxs-lookup"><span data-stu-id="1095e-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="1095e-204">Se lo strumento di merge trova una riga utilizzando DefaultValue perché lo strumento di creazione è stato rifiutato per fornire un valore.</span><span class="sxs-lookup"><span data-stu-id="1095e-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="1095e-205">msmConfigurableOptionNonNullable</span><span class="sxs-lookup"><span data-stu-id="1095e-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="1095e-206">2</span><span class="sxs-lookup"><span data-stu-id="1095e-206">2</span></span>       | <span data-ttu-id="1095e-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1095e-207">0x00000002</span></span>  | <span data-ttu-id="1095e-208">Quando si imposta questo attributo, null non è una risposta valida per questo elemento.</span><span class="sxs-lookup"><span data-stu-id="1095e-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="1095e-209">Questo attributo non ha effetto per i tipi di [formato integer](integer-format-types.md) o i [tipi di formato bit](bitfield-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="1095e-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="1095e-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="1095e-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="1095e-211">In questa colonna viene fornita una breve descrizione di questo elemento che può essere utilizzato dallo strumento di creazione nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1095e-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="1095e-212">Questa colonna potrebbe non essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="1095e-212">This column may not be localized.</span></span> <span data-ttu-id="1095e-213">Impostare questa colonna su null affinché il modulo richieda che lo strumento di creazione non esponga questa proprietà nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1095e-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="1095e-214">Lo strumento può ignorare il valore in questo campo.</span><span class="sxs-lookup"><span data-stu-id="1095e-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="1095e-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="1095e-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="1095e-216">In questa colonna viene fornita una descrizione di questo elemento che può essere utilizzato da Authoring Tool negli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1095e-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="1095e-217">Questa stringa può essere localizzata dalla trasformazione della lingua del modulo.</span><span class="sxs-lookup"><span data-stu-id="1095e-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="1095e-218">Questa colonna può essere null.</span><span class="sxs-lookup"><span data-stu-id="1095e-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="1095e-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span><span class="sxs-lookup"><span data-stu-id="1095e-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="1095e-220">In questa colonna viene fornito il nome di un file della guida (senza l'estensione chm) o un elenco delimitato da punti e virgola di spazi dei nomi della guida.</span><span class="sxs-lookup"><span data-stu-id="1095e-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="1095e-221">Questa colonna può essere null se non è disponibile alcuna guida.</span><span class="sxs-lookup"><span data-stu-id="1095e-221">This column can be null if no help is available.</span></span> <span data-ttu-id="1095e-222">Questa colonna può essere null solo se la colonna HelpKeyword è null.</span><span class="sxs-lookup"><span data-stu-id="1095e-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="1095e-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="1095e-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="1095e-224">Questa colonna fornisce una parola chiave nel file della guida o nello spazio dei nomi dalla colonna HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="1095e-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="1095e-225">L'interpretazione di questa parola chiave dipende dalla colonna HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="1095e-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="1095e-226">Questa colonna può essere null.</span><span class="sxs-lookup"><span data-stu-id="1095e-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1095e-227">Commenti</span><span class="sxs-lookup"><span data-stu-id="1095e-227">Remarks</span></span>

<span data-ttu-id="1095e-228">La tabella ModuleConfiguration viene utilizzata dai [moduli merge configurabili](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="1095e-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="1095e-229">Per creare un modulo merge configurabile è necessario Mergemod.dll 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1095e-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="1095e-230">Per garantire la compatibilità con le versioni precedenti di Mergemod.dll, è necessario aggiungere la tabella ModuleConfiguration e la [tabella ModuleSubstitution](modulesubstitution-table.md) alla [tabella ModuleIgnoreTable](moduleignoretable-table.md) di ogni modulo.</span><span class="sxs-lookup"><span data-stu-id="1095e-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="1095e-231">Convalida</span><span class="sxs-lookup"><span data-stu-id="1095e-231">Validation</span></span>

<dl>

[<span data-ttu-id="1095e-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="1095e-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1095e-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="1095e-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1095e-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="1095e-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="1095e-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="1095e-235">ICE45</span></span>](ice45.md)  
</dl>

 

 




