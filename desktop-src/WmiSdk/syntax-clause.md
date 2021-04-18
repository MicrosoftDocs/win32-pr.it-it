---
description: Contiene una clausola della sintassi che definisce i dati e il tipo per l'oggetto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Clausola SYNTAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318856"
---
# <a name="syntax-clause"></a><span data-ttu-id="9a41f-103">Clausola SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a41f-103">SYNTAX Clause</span></span>

<span data-ttu-id="9a41f-104">La macro di [tipo oggetto](object-type-macro.md) contiene una clausola della sintassi che definisce i dati e il tipo per l'oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="9a41f-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="9a41f-105">Sebbene il provider SNMP osservi le regole generali per il mapping delle clausole di sintassi, il provider segue anche le regole specifiche di diversi tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="9a41f-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="9a41f-106">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9a41f-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="9a41f-107">Le regole di mapping seguenti si applicano a tutti i tipi di dati descritti nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="9a41f-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="9a41f-108">La rappresentazione testuale della clausola della sintassi è mappata alla **\_ convenzione testuale** del qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="9a41f-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="9a41f-109">La definizione del tipo denominato nella clausola della sintassi è mappata alla **\_ sintassi dell'oggetto** qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="9a41f-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="9a41f-110">Questo mapping è diverso a seconda del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="9a41f-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="9a41f-111">Per ulteriori informazioni, vedere le descrizioni del mapping.</span><span class="sxs-lookup"><span data-stu-id="9a41f-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="9a41f-112">Il tipo SNMP usato per la codifica dei frame del protocollo SNMPv1 e SNMPv2C è mappato alla **codifica** del qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="9a41f-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="9a41f-113">Il qualificatore di proprietà CIM **CimType** contiene la rappresentazione testuale che formatta il valore del protocollo CIM sottostante.</span><span class="sxs-lookup"><span data-stu-id="9a41f-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="9a41f-114">Nella tabella seguente sono elencati i tipi di dati con regole specifiche che regolano il comportamento di mapping del provider.</span><span class="sxs-lookup"><span data-stu-id="9a41f-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="9a41f-115">Tipo di dati SNMP</span><span class="sxs-lookup"><span data-stu-id="9a41f-115">SNMP data type</span></span>                                     | <span data-ttu-id="9a41f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a41f-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a41f-117">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="9a41f-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="9a41f-118">Uno dei tipi di dati di base definiti nella struttura delle informazioni di gestione (SMI) Documents RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="9a41f-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="9a41f-119">Convenzione testuale</span><span class="sxs-lookup"><span data-stu-id="9a41f-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="9a41f-120">Definizione del tipo generata tramite l'utilizzo esplicito della macro della **convenzione testuale** SNMPv2c o generata tramite l'utilizzo di un tipo denominato.</span><span class="sxs-lookup"><span data-stu-id="9a41f-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="9a41f-121">Una convenzione testuale assegna un nome e, in alcuni casi, un intervallo di valori a un tipo di dati esistente.</span><span class="sxs-lookup"><span data-stu-id="9a41f-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="9a41f-122">Tipo denominato</span><span class="sxs-lookup"><span data-stu-id="9a41f-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="9a41f-123">Riferimento denominato a un tipo primitivo, una convenzione testuale o un tipo vincolato.</span><span class="sxs-lookup"><span data-stu-id="9a41f-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="9a41f-124">Tipo vincolato</span><span class="sxs-lookup"><span data-stu-id="9a41f-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="9a41f-125">Il tipo primitivo, il tipo denominato o la convenzione testuale che è stato vincolato da un meccanismo di subtipizzazione definito nei documenti SMI RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="9a41f-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="9a41f-126">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="9a41f-126">Primitive Type</span></span>

<span data-ttu-id="9a41f-127">Il tipo primitivo è uno dei tipi di dati di base definiti nella struttura delle informazioni di gestione (SMI) documenti RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="9a41f-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="9a41f-128">I tipi primitivi SNMP sono mappati ai tipi definiti CIM.</span><span class="sxs-lookup"><span data-stu-id="9a41f-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="9a41f-129">La tabella seguente elenca il mapping che si verifica quando la clausola della sintassi fa riferimento in modo esplicito a un tipo primitivo per SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="9a41f-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="9a41f-130">I qualificatori della **\_ convenzione testuale**, della **codifica** e della **\_ sintassi dell'oggetto** sono sempre uguali al tipo MIB e il valore predefinito è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="9a41f-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="9a41f-131">Tipo MIB</span><span class="sxs-lookup"><span data-stu-id="9a41f-131">MIB type</span></span>         | <span data-ttu-id="9a41f-132">Tipo Variant CIM</span><span class="sxs-lookup"><span data-stu-id="9a41f-132">CIM variant type</span></span> | <span data-ttu-id="9a41f-133">valore CimType</span><span class="sxs-lookup"><span data-stu-id="9a41f-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="9a41f-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9a41f-134">INTEGER</span></span>          | <span data-ttu-id="9a41f-135">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-135">VT\_I4</span></span>           | <span data-ttu-id="9a41f-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-136">**sint32**</span></span>    |
| <span data-ttu-id="9a41f-137">OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="9a41f-137">OCTETSTRING</span></span>      | <span data-ttu-id="9a41f-138">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-138">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-139">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-139">**string**</span></span>    |
| <span data-ttu-id="9a41f-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="9a41f-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="9a41f-141">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-141">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-142">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-142">**string**</span></span>    |
| <span data-ttu-id="9a41f-143">NULL</span><span class="sxs-lookup"><span data-stu-id="9a41f-143">NULL</span></span>             | <span data-ttu-id="9a41f-144">VT \_ null</span><span class="sxs-lookup"><span data-stu-id="9a41f-144">VT\_NULL</span></span>         | <span data-ttu-id="9a41f-145">Non supportato</span><span class="sxs-lookup"><span data-stu-id="9a41f-145">Not supported</span></span> |
| <span data-ttu-id="9a41f-146">IpAddress</span><span class="sxs-lookup"><span data-stu-id="9a41f-146">IpAddress</span></span>        | <span data-ttu-id="9a41f-147">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-147">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-148">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-148">**string**</span></span>    |
| <span data-ttu-id="9a41f-149">Contatore</span><span class="sxs-lookup"><span data-stu-id="9a41f-149">Counter</span></span>          | <span data-ttu-id="9a41f-150">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-150">VT\_I4</span></span>           | <span data-ttu-id="9a41f-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-151">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-152">Misuratore</span><span class="sxs-lookup"><span data-stu-id="9a41f-152">Gauge</span></span>            | <span data-ttu-id="9a41f-153">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-153">VT\_I4</span></span>           | <span data-ttu-id="9a41f-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-154">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-155">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="9a41f-155">TimeTicks</span></span>        | <span data-ttu-id="9a41f-156">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-156">VT\_I4</span></span>           | <span data-ttu-id="9a41f-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-157">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-158">Opaco</span><span class="sxs-lookup"><span data-stu-id="9a41f-158">Opaque</span></span>           | <span data-ttu-id="9a41f-159">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-159">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-160">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-160">**string**</span></span>    |
| <span data-ttu-id="9a41f-161">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="9a41f-161">NetworkAddress</span></span>   | <span data-ttu-id="9a41f-162">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-162">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-163">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-163">**string**</span></span>    |



 

<span data-ttu-id="9a41f-164">Il provider ignora la macro del tipo di oggetto quando la clausola della sintassi fa riferimento a **null**, in modo esplicito o tramite un'assegnazione di tipo denominata.</span><span class="sxs-lookup"><span data-stu-id="9a41f-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="9a41f-165">La tabella seguente elenca il mapping che si verifica quando la clausola della sintassi fa riferimento in modo esplicito a un tipo primitivo per SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="9a41f-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="9a41f-166">I qualificatori della **\_ convenzione testuale**, della **codifica** e della **\_ sintassi dell'oggetto** sono sempre uguali al tipo MIB e il valore predefinito è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="9a41f-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="9a41f-167">Tipo MIB</span><span class="sxs-lookup"><span data-stu-id="9a41f-167">MIB type</span></span>          | <span data-ttu-id="9a41f-168">Tipo Variant CIM</span><span class="sxs-lookup"><span data-stu-id="9a41f-168">CIM variant type</span></span> | <span data-ttu-id="9a41f-169">valore CimType</span><span class="sxs-lookup"><span data-stu-id="9a41f-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="9a41f-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="9a41f-170">INTEGER</span></span>           | <span data-ttu-id="9a41f-171">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-171">VT\_I4</span></span>           | <span data-ttu-id="9a41f-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-172">**sint32**</span></span>    |
| <span data-ttu-id="9a41f-173">STRINGA OTTETTO</span><span class="sxs-lookup"><span data-stu-id="9a41f-173">OCTET STRING</span></span>      | <span data-ttu-id="9a41f-174">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-174">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-175">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-175">**string**</span></span>    |
| <span data-ttu-id="9a41f-176">IDENTIFICATORE OGGETTO</span><span class="sxs-lookup"><span data-stu-id="9a41f-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="9a41f-177">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-177">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-178">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-178">**string**</span></span>    |
| <span data-ttu-id="9a41f-179">IpAddress</span><span class="sxs-lookup"><span data-stu-id="9a41f-179">IpAddress</span></span>         | <span data-ttu-id="9a41f-180">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-180">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-181">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-181">**string**</span></span>    |
| <span data-ttu-id="9a41f-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="9a41f-182">Counter32</span></span>         | <span data-ttu-id="9a41f-183">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-183">VT\_I4</span></span>           | <span data-ttu-id="9a41f-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-184">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-185">Gauge32</span><span class="sxs-lookup"><span data-stu-id="9a41f-185">Gauge32</span></span>           | <span data-ttu-id="9a41f-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-186">VT\_I4</span></span>           | <span data-ttu-id="9a41f-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-187">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="9a41f-188">Unsigned32</span></span>        | <span data-ttu-id="9a41f-189">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-189">VT\_I4</span></span>           | <span data-ttu-id="9a41f-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-190">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="9a41f-191">Integer32</span></span>         | <span data-ttu-id="9a41f-192">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-192">VT\_I4</span></span>           | <span data-ttu-id="9a41f-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-193">**sint32**</span></span>    |
| <span data-ttu-id="9a41f-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="9a41f-194">Counter64</span></span>         | <span data-ttu-id="9a41f-195">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-195">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="9a41f-196">**uint64**</span></span>    |
| <span data-ttu-id="9a41f-197">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="9a41f-197">TimeTicks</span></span>         | <span data-ttu-id="9a41f-198">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9a41f-198">VT\_I4</span></span>           | <span data-ttu-id="9a41f-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="9a41f-199">**uint32**</span></span>    |
| <span data-ttu-id="9a41f-200">Opaco</span><span class="sxs-lookup"><span data-stu-id="9a41f-200">Opaque</span></span>            | <span data-ttu-id="9a41f-201">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-201">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-202">**string**</span><span class="sxs-lookup"><span data-stu-id="9a41f-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="9a41f-203">Tipo denominato</span><span class="sxs-lookup"><span data-stu-id="9a41f-203">Named Type</span></span>

<span data-ttu-id="9a41f-204">I tipi denominati SNMP vengono mappati ai tipi definiti CIM.</span><span class="sxs-lookup"><span data-stu-id="9a41f-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="9a41f-205">Quando la clausola della sintassi fa riferimento a un [tipo primitivo](#primitive-type), a una [convenzione testuale](textual-convention-macro.md)o a un [tipo vincolato](#constrained-type) tramite una derivazione di assegnazione del tipo, utilizzare tali tipi per determinare quali procedure di mapping applicare.</span><span class="sxs-lookup"><span data-stu-id="9a41f-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="9a41f-206">Se, tramite la derivazione delle regole di assegnazione del tipo, si verifica una definizione di tipo vincolato:</span><span class="sxs-lookup"><span data-stu-id="9a41f-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="9a41f-207">Se, tramite un'ulteriore derivazione, si verifica una delle convenzioni testuali elencate nella [macro della convenzione testuale](textual-convention-macro.md), applicare le regole di mapping per i tipi vincolati e le convenzioni testuali.</span><span class="sxs-lookup"><span data-stu-id="9a41f-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="9a41f-208">In caso contrario, se si riscontra uno dei tipi primitivi elencati in una tabella di tipi primitivi, applicare le regole di mapping per i tipi primitivi e i tipi vincolati.</span><span class="sxs-lookup"><span data-stu-id="9a41f-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="9a41f-209">Se si verifica una delle convenzioni testuali elencate nella [ \_ macro della convenzione testuale](textual-convention-macro.md), applicare le regole di mapping per le convenzioni testuali.</span><span class="sxs-lookup"><span data-stu-id="9a41f-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="9a41f-210">Se si riscontra uno dei tipi primitivi elencati in una tabella di tipo primitiva, applicare le regole di mapping per i tipi primitivi.</span><span class="sxs-lookup"><span data-stu-id="9a41f-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="9a41f-211">Le classi che contengono tipi di proprietà che non sono conformi al mapping descritto in precedenza non sono valide.</span><span class="sxs-lookup"><span data-stu-id="9a41f-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="9a41f-212">In questo caso, il provider restituisce un errore se e quando il provider richiede il recupero di una definizione di classe durante l'esecuzione di una funzione di recupero dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9a41f-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="9a41f-213">Tipo vincolato</span><span class="sxs-lookup"><span data-stu-id="9a41f-213">Constrained Type</span></span>

<span data-ttu-id="9a41f-214">Un tipo vincolato è un tipo primitivo, un tipo denominato o una convenzione testuale che è stata vincolata da un meccanismo di sottotipizzazione definito nei documenti SMI RFC 1213 e RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="9a41f-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="9a41f-215">Quando si verifica la sottotipizzazione, per specificare i valori dei sottotipi sono necessari qualificatori CIM aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9a41f-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="9a41f-216">La definizione del tipo denominato nella clausola della sintassi esegue il mapping Verbatim alla sintassi dell' **oggetto \_** qualificatore della proprietà CIM fino a, ma non include i vincoli del sottotipo.</span><span class="sxs-lookup"><span data-stu-id="9a41f-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="9a41f-217">I sottotipi possono seguire uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a41f-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="9a41f-218">INTEGER enumerato</span><span class="sxs-lookup"><span data-stu-id="9a41f-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="9a41f-219">L' **enumerazione** CIM Property Qualifier specifica i valori enumerati.</span><span class="sxs-lookup"><span data-stu-id="9a41f-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="9a41f-220">Questo qualificatore è rappresentato come stringa contenente un elenco delimitato da virgole di valori interi con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9a41f-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="9a41f-221">Nella tabella seguente sono elencati i tipi di mapping.</span><span class="sxs-lookup"><span data-stu-id="9a41f-221">The following table lists the mapping types.</span></span> <span data-ttu-id="9a41f-222">Il valore predefinito è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="9a41f-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="9a41f-223">Tipo MIB vincolato</span><span class="sxs-lookup"><span data-stu-id="9a41f-223">Constrained MIB type</span></span> | <span data-ttu-id="9a41f-224">Tipo Variant CIM</span><span class="sxs-lookup"><span data-stu-id="9a41f-224">CIM variant type</span></span> | <span data-ttu-id="9a41f-225">Qualificatori CIM</span><span class="sxs-lookup"><span data-stu-id="9a41f-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a41f-226">INTEGER enumerato</span><span class="sxs-lookup"><span data-stu-id="9a41f-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="9a41f-227">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-227">VT\_BSTR</span></span>         | <span data-ttu-id="9a41f-228">**\_ convenzione testuale**: enumeratedinteger</span><span class="sxs-lookup"><span data-stu-id="9a41f-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="9a41f-229">**codifica**: integer</span><span class="sxs-lookup"><span data-stu-id="9a41f-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="9a41f-230">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="9a41f-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="9a41f-231">BITS</span><span class="sxs-lookup"><span data-stu-id="9a41f-231">BITS</span></span>

    <span data-ttu-id="9a41f-232">I **bit** del qualificatore della proprietà CIM specificano i valori enumerati.</span><span class="sxs-lookup"><span data-stu-id="9a41f-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="9a41f-233">Questo qualificatore è rappresentato come stringa contenente un elenco delimitato da virgole di valori interi con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9a41f-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="9a41f-234">Nella tabella seguente sono elencati i tipi di mapping.</span><span class="sxs-lookup"><span data-stu-id="9a41f-234">The following table lists the mapping types.</span></span> <span data-ttu-id="9a41f-235">Il valore predefinito è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="9a41f-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="9a41f-236">Tipo MIB vincolato</span><span class="sxs-lookup"><span data-stu-id="9a41f-236">Constrained MIB type</span></span> | <span data-ttu-id="9a41f-237">Tipo Variant CIM</span><span class="sxs-lookup"><span data-stu-id="9a41f-237">CIM variant type</span></span>      | <span data-ttu-id="9a41f-238">Qualificatori CIM</span><span class="sxs-lookup"><span data-stu-id="9a41f-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a41f-239">BITS</span><span class="sxs-lookup"><span data-stu-id="9a41f-239">BITS</span></span>                 | <span data-ttu-id="9a41f-240">\_ \| VT BSTR matrice \_ VT</span><span class="sxs-lookup"><span data-stu-id="9a41f-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="9a41f-241">**\_ convenzione testuale**: BITS</span><span class="sxs-lookup"><span data-stu-id="9a41f-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="9a41f-242">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="9a41f-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="9a41f-243">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="9a41f-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="9a41f-244">A lunghezza variabile</span><span class="sxs-lookup"><span data-stu-id="9a41f-244">Variable-length</span></span>

    <span data-ttu-id="9a41f-245">Quando la clausola della sintassi fa riferimento a un tipo primitivo, a un tipo denominato o a una convenzione testuale sottoposta a una stringa di ottetto a lunghezza variabile o opaca, la **\_ lunghezza variabile** del qualificatore di proprietà CIM specifica i valori minimo, massimo e a lunghezza fissa associati alla definizione del tipo.</span><span class="sxs-lookup"><span data-stu-id="9a41f-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="9a41f-246">Questo qualificatore viene implementato come stringa nel formato seguente, in cui i valori a lunghezza variabile sono rappresentati come interi senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9a41f-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="9a41f-247">A lunghezza fissa</span><span class="sxs-lookup"><span data-stu-id="9a41f-247">Fixed-length</span></span>

    <span data-ttu-id="9a41f-248">Quando la clausola della sintassi fa riferimento a un tipo primitivo, a un tipo denominato o a una convenzione testuale sottoposta a una stringa di ottetto a lunghezza fissa o opaca, la **\_ lunghezza fissa** del qualificatore di proprietà CIM specifica il valore a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="9a41f-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="9a41f-249">Questo qualificatore è rappresentato come valore intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9a41f-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="9a41f-250">Range</span><span class="sxs-lookup"><span data-stu-id="9a41f-250">Range</span></span>

    <span data-ttu-id="9a41f-251">Quando la clausola della sintassi fa riferimento a un tipo primitivo, a un tipo denominato o a una convenzione testuale sottoposta a un numero intero o a un misuratore a valore fisso o a intervalli, il **\_ valore della variabile** del qualificatore della proprietà CIM specifica i valori a intervalli e fissi associati alla definizione del tipo.</span><span class="sxs-lookup"><span data-stu-id="9a41f-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="9a41f-252">Questo qualificatore viene implementato come stringa nel formato seguente, in cui i valori di intervallo e di lunghezza fissa sono rappresentati come interi senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9a41f-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="9a41f-253">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="9a41f-253">Example Code</span></span>

<span data-ttu-id="9a41f-254">Nell'esempio seguente viene descritto un sottotipo INTEGER enumerato.</span><span class="sxs-lookup"><span data-stu-id="9a41f-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="9a41f-255">Questo esempio esegue il mapping a:</span><span class="sxs-lookup"><span data-stu-id="9a41f-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="9a41f-256">Nell'esempio di codice riportato di seguito viene descritto un sottotipo BITS.</span><span class="sxs-lookup"><span data-stu-id="9a41f-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="9a41f-257">Nell'esempio di codice seguente viene eseguito il mapping a:</span><span class="sxs-lookup"><span data-stu-id="9a41f-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="9a41f-258">Nell'esempio di codice riportato di seguito viene descritto un sottotipo a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="9a41f-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="9a41f-259">Questo esempio esegue il mapping a:</span><span class="sxs-lookup"><span data-stu-id="9a41f-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="9a41f-260">Nell'esempio seguente viene descritto un sottotipo a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="9a41f-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="9a41f-261">Questo esempio esegue il mapping a:</span><span class="sxs-lookup"><span data-stu-id="9a41f-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="9a41f-262">Nell'esempio seguente viene descritto un sottotipo di intervallo.</span><span class="sxs-lookup"><span data-stu-id="9a41f-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="9a41f-263">Questo esempio esegue il mapping a:</span><span class="sxs-lookup"><span data-stu-id="9a41f-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 




