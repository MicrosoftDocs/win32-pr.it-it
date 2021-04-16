---
title: Livello di supporto dello schema
description: In questa sezione vengono illustrati i dettagli relativi al livello di supporto dello schema.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Servizi Web a livello di supporto dello schema per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104571266"
---
# <a name="schema-support-level"></a><span data-ttu-id="2e1e6-106">Livello di supporto dello schema</span><span class="sxs-lookup"><span data-stu-id="2e1e6-106">Schema support level</span></span>

<span data-ttu-id="2e1e6-107">In questa sezione vengono illustrati i dettagli relativi al livello di supporto dello schema.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="2e1e6-108">Lo schema supporta direttamente gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e1e6-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="2e1e6-109">Sequenze di elementi.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-109">Sequences of elements.</span></span>
-   <span data-ttu-id="2e1e6-110">Derivazione di tipi di elemento.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-110">Derivation of element types.</span></span>
-   <span data-ttu-id="2e1e6-111">Scelte semplici di elementi (quelli che vengono mappati a un'Unione con tag).</span><span class="sxs-lookup"><span data-stu-id="2e1e6-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="2e1e6-112">Tipi di base definiti dal formato binario XSD/.NET, inclusi gli intervalli (min/max).</span><span class="sxs-lookup"><span data-stu-id="2e1e6-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="2e1e6-113">Supporto semplice per qualsiasi elemento (nessuna restrizione sul tipo di elemento).</span><span class="sxs-lookup"><span data-stu-id="2e1e6-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="2e1e6-114">Elementi e attributi facoltativi con valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="2e1e6-115">Ripetizione di elementi con intervalli (min/max).</span><span class="sxs-lookup"><span data-stu-id="2e1e6-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="2e1e6-116">Elementi nillable.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-116">Nillable elements.</span></span>

<span data-ttu-id="2e1e6-117">Lo schema non supporta direttamente le operazioni seguenti, che implicano il comportamento di fallback:</span><span class="sxs-lookup"><span data-stu-id="2e1e6-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="2e1e6-118">Tipi di base definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-118">User defined basic types.</span></span>
-   <span data-ttu-id="2e1e6-119">Scelte più complesse.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-119">More complicated choices.</span></span>
-   <span data-ttu-id="2e1e6-120">Rifiuto degli attributi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="2e1e6-121">Arrotondamento degli attributi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="2e1e6-122">Supporto più complesso per qualsiasi elemento.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="2e1e6-123">Costrutto all.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-123">The all construct.</span></span>
-   <span data-ttu-id="2e1e6-124">Chiave/keyref.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-124">Key/keyref.</span></span>

<span data-ttu-id="2e1e6-125">Di seguito è riportata una suddivisione dettagliata del supporto dei diversi componenti dello schema.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="2e1e6-126">Viene confrontato con il contratto dati in WCF perché la somiglianza della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="2e1e6-127">La differenza verrà descritta.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-127">The difference will be described.</span></span>

<span data-ttu-id="2e1e6-128">In genere, per i comportamenti di fallback:</span><span class="sxs-lookup"><span data-stu-id="2e1e6-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="2e1e6-129">viene eseguito il fallback degli attributi a WS \_ String;</span><span class="sxs-lookup"><span data-stu-id="2e1e6-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="2e1e6-130">viene eseguito il fallback del contenuto dell'elemento \_ nel \_ buffer WS XML.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-131">viene eseguito il fallback di complexType alla struttura contenente un campo del \_ buffer WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-132">Per i tipi semplici viene eseguito il fallback a WS \_ String.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="2e1e6-133">wsutil genera avvisi per i componenti dello schema che attualmente non sono completamente supportati.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="2e1e6-134">È necessario che l'applicazione esegua una verifica aggiuntiva per questi componenti.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="2e1e6-135">È possibile migliorare il WSUTIL di lavoro straordinario per gestire alcune delle funzionalità attualmente supportate in fase di esecuzione, ad esempio il supporto dei valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="2e1e6-136">wsutil può anche essere migliorato insieme alla serializzazione per supportare altre funzionalità, ad esempio abstract.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="2e1e6-137">Il numero di componenti dello schema non supportati può essere ridotto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="2e1e6-138">Documento dello schema generale</span><span class="sxs-lookup"><span data-stu-id="2e1e6-138">The Overall Schema Document</span></span>

<span data-ttu-id="2e1e6-139">Definizione globale che può influire sulle definizioni incorporate nello schema.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="2e1e6-140">Si tratta di attributi globali applicabili a tutte le definizioni nello schema.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="2e1e6-141"><XS: Schema> attributi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="2e1e6-142">attributeFromDefault ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="2e1e6-143">blockDefault ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="2e1e6-144">elementFormDefault ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="2e1e6-145">Questa operazione è diversa rispetto a DataContract perché gli elementi non qualificati sono supportati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="2e1e6-146">finalDefault ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-146">finalDefault Ignored.</span></span> <span data-ttu-id="2e1e6-147">Non è disponibile alcun supporto per il linguaggio C per il concetto di Final.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="2e1e6-148">ID ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-148">id Ignored.</span></span>
-   <span data-ttu-id="2e1e6-149">targetNamespace supportato e mappato allo spazio dei nomi del servizio.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="2e1e6-150">versione ignorata.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-150">version Ignored.</span></span>

<span data-ttu-id="2e1e6-151"><XS: contenuto del> dello schema</span><span class="sxs-lookup"><span data-stu-id="2e1e6-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="2e1e6-152">includere supportato; wsutil richiede che tutte le definizioni necessarie siano disponibili come file di input in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="2e1e6-153">ridefinizione ignorata.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-153">redefine Ignored.</span></span> <span data-ttu-id="2e1e6-154">wsutil non supporta questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="2e1e6-155">importazione supportata. wsutil richiede che tutte le definizioni necessarie siano disponibili come file di input in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="2e1e6-156">simpleType supportato. vedere la sezione di tipo semplice riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="2e1e6-157">complexType supportato: vedere la sezione ' complexType '</span><span class="sxs-lookup"><span data-stu-id="2e1e6-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="2e1e6-158">gruppo ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-158">group Ignored.</span></span>
-   <span data-ttu-id="2e1e6-159">attributeGroup ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="2e1e6-160">elemento supportato; esegue il mapping a definizioni di elementi globali.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="2e1e6-161">attributo supportato; esegue il mapping alle definizioni degli attributi globali.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="2e1e6-162">notazione ignorata</span><span class="sxs-lookup"><span data-stu-id="2e1e6-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="2e1e6-163">Tipo complesso</span><span class="sxs-lookup"><span data-stu-id="2e1e6-163">Complex Type</span></span>

<span data-ttu-id="2e1e6-164">Il tipo complesso, rappresentato da <XS: complexType>, potrebbe essere una restrizione di tipo semplice o complesso, estensione di tipo semplice, matrici o struttura.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="2e1e6-165">Si è notato che nell'estensione di tipi semplici non sono presenti ereditarietà né supporto xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="2e1e6-166"><XS: complexType> attributi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="2e1e6-167">abstract genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-168">blocca genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-169">Genera avviso finale per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-170">ID ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-170">id Ignored.</span></span>
-   <span data-ttu-id="2e1e6-171">Genera un avviso misto per la funzionalità non supportata, il fallback alla struttura con il \_ buffer WS XML \_ Se true.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="2e1e6-172">nome supportato e mappato al nome del tipo di struttura.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="2e1e6-173"><XS: complexType> contenuto</span><span class="sxs-lookup"><span data-stu-id="2e1e6-173"><xs:complexType> contents</span></span>

<span data-ttu-id="2e1e6-174">Si tratta della definizione di tipo per la struttura.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-174">This is type definition for structure.</span></span> <span data-ttu-id="2e1e6-175">la restrizione complexContent non è supportata.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="2e1e6-176">complexContent supporta l'estensione di contenuto complesso.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="2e1e6-177">Esegue il mapping all'ereditarietà della struttura.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="2e1e6-178">raggruppa attualmente il fallback alla struttura con \_ il \_ campo del buffer WS XML.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="2e1e6-179">Può essere supportato in base alla particella sottostante.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="2e1e6-180">scelta supportata come Unione.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-180">choice supported as union.</span></span> <span data-ttu-id="2e1e6-181">Questa operazione non è supportata nel contratto dati.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="2e1e6-182">sequenza supportata: esegue il mapping ai campi di una struttura</span><span class="sxs-lookup"><span data-stu-id="2e1e6-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="2e1e6-183">l'attributo è supportato con un'eccezione di ' proibito '.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="2e1e6-184">fallback alla struttura con il \_ buffer WS XML \_ se è vietato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="2e1e6-185">supportato da attributeGroup: esegue il mapping a una sequenza di attributi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="2e1e6-186">anyAttribute ignorato</span><span class="sxs-lookup"><span data-stu-id="2e1e6-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="2e1e6-187">AttributeGroupRef supportato: esegue il mapping a una sequenza di attributi.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="2e1e6-188">GroupRef attualmente il fallback alla struttura con \_ il \_ campo del buffer WS XML.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="2e1e6-189">Può essere supportato in base al gruppo sottostante.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="2e1e6-190">Qualsiasi supportato, esegue il mapping al \_ buffer XML</span><span class="sxs-lookup"><span data-stu-id="2e1e6-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="2e1e6-191">(blank) il mapping supportato alla descrizione di struct vuota senza struct è stato generato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="2e1e6-192"><xs:sequence> in un tipo complesso: contenuto</span><span class="sxs-lookup"><span data-stu-id="2e1e6-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="2e1e6-193">wsutil supporta completamente la sequenza di minOccurs = 1 e maxOccurs = 1; in caso contrario, il tipo complesso è attualmente associato al \_ buffer WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="2e1e6-194">Può essere supportata come matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="2e1e6-195">elemento supportato; ogni istanza esegue il mapping a un campo nella struttura.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="2e1e6-196">Fallback del gruppo; complexType è il fallback al \_ buffer WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-197">Tutti i fallback; complexType è il fallback al \_ buffer WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-198">scelta supportata. eseguire il mapping al campo Union.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="2e1e6-199">fallback sequenza; complexType è il fallback al \_ buffer WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-200">qualsiasi supportato; mappato al \_ buffer XML.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-201">(blank) supportato; complexType può essere una struttura vuota se non sono presenti attributi.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="2e1e6-202">Elementi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-202">Elements</span></span>

<span data-ttu-id="2e1e6-203"><XS: element>può verificarsi in tre contesti.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="2e1e6-204">Può verificarsi all'interno di un <XS: Sequence>, che descrive un campo di uno struct normale.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="2e1e6-205">In questo caso, l'attributo maxOccurs deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="2e1e6-206">Il campo è facoltativo se minOccurs è 0.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="2e1e6-207">Può verificarsi all'interno di un <XS: Sequence>, che descrive un campo di una matrice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="2e1e6-208">In questo caso, l'attributo maxOccurs deve essere maggiore di 1 o "unbounded".</span><span class="sxs-lookup"><span data-stu-id="2e1e6-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="2e1e6-209">Potrebbe verificarsi in un <XS: Schema> come descrizione dell'elemento globale.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="2e1e6-210"><XS: element> all'interno di un <XS: Sequence> o <XS: Choice> come campo in una struttura</span><span class="sxs-lookup"><span data-stu-id="2e1e6-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="2e1e6-211">Ref supportato; il riferimento all'elemento globale è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="2e1e6-212">nome supportato, esegue il mapping a nome campo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="2e1e6-213">tipo supportato, esegue il mapping al tipo di campo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-213">type Supported, maps to field type.</span></span> <span data-ttu-id="2e1e6-214">Per ulteriori informazioni, vedere "mapping dei tipi".</span><span class="sxs-lookup"><span data-stu-id="2e1e6-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="2e1e6-215">Se non è specificato (e l'elemento non contiene un tipo anonimo), viene utilizzato XS: anyType.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="2e1e6-216">blocca genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-217">impostazione predefinita genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-218">correzione di genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-219">Form ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-219">form Ignored.</span></span> <span data-ttu-id="2e1e6-220">Il livello di serializzazione supporta sia moduli qualificati che non qualificati.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="2e1e6-221">ID ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-221">id Ignored.</span></span>
-   <span data-ttu-id="2e1e6-222">maxOccurs esegue il mapping a un singolo campo dati se è uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="2e1e6-223">viene mappato a un campo di matrice (elemento ripetuto) se maxOccurs è maggiore di 1.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="2e1e6-224">minOccurs se 0, il campo opzioni è impostato su campo \_ facoltativo, se nillable non è impostato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="2e1e6-225">nillable il campo è nillable.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-225">nillable The field is nillable.</span></span> <span data-ttu-id="2e1e6-226">Per ulteriori informazioni, vedere [serializzazione](serialization.md) .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="2e1e6-227"><XS: element> come elemento globale: attributi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="2e1e6-228">gli attributi minOccurs e maxOccurs non sono validi come descrizione dell'elemento globale.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="2e1e6-229">L'applicazione può usare direttamente la descrizione dell'elemento generato nei livelli di serializzazione o del canale.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="2e1e6-230">abstract genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-231">blocca genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-232">impostazione predefinita genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-233">Genera avviso finale per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-234">correzione di genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-235">ID ignorato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-235">id Ignored.</span></span>
-   <span data-ttu-id="2e1e6-236">nome supportato: esegue il mapping al nome della descrizione dell'elemento globale ed è la base per il tipo anonimo quando specificato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="2e1e6-237">nillable ignorato: l'applicazione deve chiamare con il flag right.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="2e1e6-238">substitutionGroup il fallback alla struttura con \_ il \_ buffer WS XML, se impostato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="2e1e6-239">wsutil non supporta substitutionGroup.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="2e1e6-240">tipo supportato e mappato al tipo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="2e1e6-241"><XS: element> come elemento globale: Contents</span><span class="sxs-lookup"><span data-stu-id="2e1e6-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="2e1e6-242">simpleType supportato; esegue il mapping alla definizione del tipo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="2e1e6-243">complexType supportato; esegue il mapping a un tipo complesso.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="2e1e6-244">Genera un avviso univoco sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="2e1e6-245">wsutil non supporta vincoli di elemento.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="2e1e6-246">chiave genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="2e1e6-247">wsutil non supporta vincoli di elemento.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="2e1e6-248">keyref genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="2e1e6-249">wsutil non supporta vincoli di elemento.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="2e1e6-250">vuoto Supportato l'elemento senza specifica del tipo viene trattato come xs: anyType.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="2e1e6-251">Tipi semplici</span><span class="sxs-lookup"><span data-stu-id="2e1e6-251">Simple Types</span></span>

<span data-ttu-id="2e1e6-252"><XS: simpleType> attributi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="2e1e6-253">Genera avviso finale per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-254">ID ignorato</span><span class="sxs-lookup"><span data-stu-id="2e1e6-254">Id Ignored</span></span>
-   <span data-ttu-id="2e1e6-255">Nome supportato, mappato al nome del tipo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="2e1e6-256"><XS: simpleType> contenuto</span><span class="sxs-lookup"><span data-stu-id="2e1e6-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="2e1e6-257">Restrizione supportata, esegue il mapping a un tipo enum o a un intervallo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="2e1e6-258">Vedere la sezione relativa alle restrizioni xs: simpleType.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="2e1e6-259">Elenco genera avviso per funzionalità non supportate, fallback al buffer XML \_ .</span><span class="sxs-lookup"><span data-stu-id="2e1e6-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="2e1e6-260">Unione genera avviso per la funzionalità non supportata, fallback al \_ buffer XML.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="2e1e6-261">Restrizione di tipo semplice</span><span class="sxs-lookup"><span data-stu-id="2e1e6-261">Simple Type restriction</span></span>

<span data-ttu-id="2e1e6-262">Alcuni facet sono consentiti in tipi integrali e tipo di stringhe per consentire il supporto di intervalli e enum.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="2e1e6-263">supporto dell'enumerazione</span><span class="sxs-lookup"><span data-stu-id="2e1e6-263">enumeration support</span></span>

<span data-ttu-id="2e1e6-264"><XS: Enumeration> restrizione di tipo semplice per il tipo di base della stringa viene considerata come un tipo enum.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="2e1e6-265">In questo caso, l'attributo di base deve essere di tipo stringa.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="2e1e6-266">In caso di enumerazione, tutti gli altri facet vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="2e1e6-267">intervallo con supporto di tipi semplici</span><span class="sxs-lookup"><span data-stu-id="2e1e6-267">range on simple type support</span></span>

<span data-ttu-id="2e1e6-268">Alcuni facet sono supportati nei tipi semplici. il supporto di un intervallo consentito per il tipo è efficace.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="2e1e6-269">Di seguito sono riportate le restrizioni per i tipi integrali e i tipi float/double.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="2e1e6-270">Per i tipi semplici con altri facet viene eseguito il fallback al \_ tipo di stringa WS</span><span class="sxs-lookup"><span data-stu-id="2e1e6-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="2e1e6-271">minExclusive supportato</span><span class="sxs-lookup"><span data-stu-id="2e1e6-271">minExclusive Supported</span></span>
-   <span data-ttu-id="2e1e6-272">minInclusive supportato</span><span class="sxs-lookup"><span data-stu-id="2e1e6-272">minInclusive Supported</span></span>
-   <span data-ttu-id="2e1e6-273">maxExclusive supportato</span><span class="sxs-lookup"><span data-stu-id="2e1e6-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="2e1e6-274">maxInclusive supportato</span><span class="sxs-lookup"><span data-stu-id="2e1e6-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="2e1e6-275">totalDigits genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-276">fractionDigits genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-277">la lunghezza genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-278">minLength genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-279">maxLength genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-280">l'enumerazione genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-281">gli spazi vuoti generano un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-282">modello genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="2e1e6-283">vuoto Supportato.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-283">(blank) Supported.</span></span>

<span data-ttu-id="2e1e6-284">minLength e maxLength in una stringa non sono attualmente supportati, ma è una funzionalità auspicabile da supportare.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="2e1e6-285">Ereditarietà</span><span class="sxs-lookup"><span data-stu-id="2e1e6-285">Inheritance</span></span>

<span data-ttu-id="2e1e6-286">Wsutil supporta l'ereditarietà di tipi complessi, ovvero una struttura può ereditare da un'altra struttura, in modo analogo all'ereditarietà dell'interfaccia in C++.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="2e1e6-287">Questa operazione viene eseguita tramite <XS: complexContentExtension>.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="2e1e6-288"><XS: simpleContentExtension> è supportato, ma viene generato come struttura normale con tipo di base come primo campo anziché come ereditarietà del tipo.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="2e1e6-289">Mapping di tipi/primitivi</span><span class="sxs-lookup"><span data-stu-id="2e1e6-289">Type/primitive mapping</span></span>

<span data-ttu-id="2e1e6-290">È necessario normalizzare gli identificatori quando si esegue la conversione da un NCName in XML.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="2e1e6-291">Le stringhe sono nillable; i tipi di puntatore sono nillable; i tipi integrali e float/double sono nillable e defaultValue è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="2e1e6-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![Tabella che mostra il mapping tra i tipi XSD e i tipi di dati Sapphire.](images/schematypemap.png)

 

 




