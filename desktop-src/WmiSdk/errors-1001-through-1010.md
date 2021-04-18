---
description: Descrive gli errori del provider SNMP WMI da 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Errori da 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313191"
---
# <a name="errors-1001-through-1010"></a><span data-ttu-id="b8362-103">Errori da 1001 a 1010</span><span class="sxs-lookup"><span data-stu-id="b8362-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="b8362-104">Descrive gli errori del provider SNMP WMI da 1001 a 1010.</span><span class="sxs-lookup"><span data-stu-id="b8362-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="b8362-105">Errore irreversibile 1001</span><span class="sxs-lookup"><span data-stu-id="b8362-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="b8362-106">Errore irreversibile 1002</span><span class="sxs-lookup"><span data-stu-id="b8362-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="b8362-107">Errore irreversibile 1003</span><span class="sxs-lookup"><span data-stu-id="b8362-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="b8362-108">Avviso 1004</span><span class="sxs-lookup"><span data-stu-id="b8362-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="b8362-109">Avviso 1005</span><span class="sxs-lookup"><span data-stu-id="b8362-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="b8362-110">Errore irreversibile 1006</span><span class="sxs-lookup"><span data-stu-id="b8362-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="b8362-111">Errore irreversibile 1008</span><span class="sxs-lookup"><span data-stu-id="b8362-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="b8362-112">Errore irreversibile 1001</span><span class="sxs-lookup"><span data-stu-id="b8362-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="b8362-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001,> irreversibile: " <fileName> : <riga \#>: la clausola della sintassi di tipo oggetto non viene risolta nei tipi consentiti"</span><span class="sxs-lookup"><span data-stu-id="b8362-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="b8362-114">Errore semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="b8362-115">La clausola SYNTAX della macro del tipo di oggetto deve essere risolta in un tipo o sottotipo, formato utilizzando la specifica di dimensione o intervallo consentita da SNMPv1 o SNMPv2C SMI.</span><span class="sxs-lookup"><span data-stu-id="b8362-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="b8362-116">In caso contrario, viene restituito l'errore irreversibile 1001.</span><span class="sxs-lookup"><span data-stu-id="b8362-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="b8362-117">Questo errore può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b8362-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="b8362-118">I tipi consentiti da SNMPv1 SMI sono:</span><span class="sxs-lookup"><span data-stu-id="b8362-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="b8362-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="b8362-119">INTEGER</span></span>
-   <span data-ttu-id="b8362-120">NULL</span><span class="sxs-lookup"><span data-stu-id="b8362-120">NULL</span></span>
-   <span data-ttu-id="b8362-121">STRINGA OTTETTO</span><span class="sxs-lookup"><span data-stu-id="b8362-121">OCTET STRING</span></span>
-   <span data-ttu-id="b8362-122">IDENTIFICATORE OGGETTO</span><span class="sxs-lookup"><span data-stu-id="b8362-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="b8362-123">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="b8362-123">NetworkAddress</span></span>
-   <span data-ttu-id="b8362-124">IpAddress</span><span class="sxs-lookup"><span data-stu-id="b8362-124">IpAddress</span></span>
-   <span data-ttu-id="b8362-125">Contatore</span><span class="sxs-lookup"><span data-stu-id="b8362-125">Counter</span></span>
-   <span data-ttu-id="b8362-126">Misuratore</span><span class="sxs-lookup"><span data-stu-id="b8362-126">Gauge</span></span>
-   <span data-ttu-id="b8362-127">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="b8362-127">TimeTicks</span></span>
-   <span data-ttu-id="b8362-128">Opaco</span><span class="sxs-lookup"><span data-stu-id="b8362-128">Opaque</span></span>
-   <span data-ttu-id="b8362-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="b8362-129">DisplayString</span></span>
-   <span data-ttu-id="b8362-130">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="b8362-130">PhysAddress</span></span>

<span data-ttu-id="b8362-131">I tipi consentiti da SNMPv2C SMI sono:</span><span class="sxs-lookup"><span data-stu-id="b8362-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="b8362-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="b8362-132">INTEGER</span></span>
-   <span data-ttu-id="b8362-133">STRINGA OTTETTO</span><span class="sxs-lookup"><span data-stu-id="b8362-133">OCTET STRING</span></span>
-   <span data-ttu-id="b8362-134">IDENTIFICATORE OGGETTO</span><span class="sxs-lookup"><span data-stu-id="b8362-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="b8362-135">BITS</span><span class="sxs-lookup"><span data-stu-id="b8362-135">BITS</span></span>
-   <span data-ttu-id="b8362-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="b8362-136">Integer32</span></span>
-   <span data-ttu-id="b8362-137">IpAddress</span><span class="sxs-lookup"><span data-stu-id="b8362-137">IpAddress</span></span>
-   <span data-ttu-id="b8362-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="b8362-138">Counter32</span></span>
-   <span data-ttu-id="b8362-139">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="b8362-139">TimeTicks</span></span>
-   <span data-ttu-id="b8362-140">Opaco</span><span class="sxs-lookup"><span data-stu-id="b8362-140">Opaque</span></span>
-   <span data-ttu-id="b8362-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="b8362-141">Counter64</span></span>
-   <span data-ttu-id="b8362-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="b8362-142">Unsigned32</span></span>
-   <span data-ttu-id="b8362-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="b8362-143">DisplayString</span></span>
-   <span data-ttu-id="b8362-144">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="b8362-144">PhysAddress</span></span>
-   <span data-ttu-id="b8362-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="b8362-145">MacAddress</span></span>
-   <span data-ttu-id="b8362-146">TruthValue</span><span class="sxs-lookup"><span data-stu-id="b8362-146">TruthValue</span></span>
-   <span data-ttu-id="b8362-147">TestAndIncr</span><span class="sxs-lookup"><span data-stu-id="b8362-147">TestAndIncr</span></span>
-   <span data-ttu-id="b8362-148">AutonomousType</span><span class="sxs-lookup"><span data-stu-id="b8362-148">AutonomousType</span></span>
-   <span data-ttu-id="b8362-149">InstancePointer</span><span class="sxs-lookup"><span data-stu-id="b8362-149">InstancePointer</span></span>
-   <span data-ttu-id="b8362-150">VariablePointer</span><span class="sxs-lookup"><span data-stu-id="b8362-150">VariablePointer</span></span>
-   <span data-ttu-id="b8362-151">RowPointer</span><span class="sxs-lookup"><span data-stu-id="b8362-151">RowPointer</span></span>
-   <span data-ttu-id="b8362-152">RowStatus</span><span class="sxs-lookup"><span data-stu-id="b8362-152">RowStatus</span></span>
-   <span data-ttu-id="b8362-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="b8362-153">TimeStamp</span></span>
-   <span data-ttu-id="b8362-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="b8362-154">TimeInterval</span></span>
-   <span data-ttu-id="b8362-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="b8362-155">DateAndTime</span></span>
-   <span data-ttu-id="b8362-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="b8362-156">StorageType</span></span>
-   <span data-ttu-id="b8362-157">Tdomain</span><span class="sxs-lookup"><span data-stu-id="b8362-157">Tdomain</span></span>
-   <span data-ttu-id="b8362-158">Taddress</span><span class="sxs-lookup"><span data-stu-id="b8362-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="b8362-159">Errore irreversibile 1002</span><span class="sxs-lookup"><span data-stu-id="b8362-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="b8362-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> irreversibile: " <fileName> : <riga \#>: clausola di accesso non valida <clause> "</span><span class="sxs-lookup"><span data-stu-id="b8362-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="b8362-161">Errore semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="b8362-162">Per SNMPv1, la clausola ACCESS della macro del tipo di oggetto deve essere di sola lettura, "" sola scrittura "," lettura/scrittura "o" non accessibile ".</span><span class="sxs-lookup"><span data-stu-id="b8362-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="b8362-163">Per SNMPv2C, la clausola MAX-ACCESS deve essere di sola lettura, "Read-create", "Read/Write" o "non accessibile".</span><span class="sxs-lookup"><span data-stu-id="b8362-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="b8362-164">Errore irreversibile 1003</span><span class="sxs-lookup"><span data-stu-id="b8362-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="b8362-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> irreversibile: " <fileName> : <riga \#>: clausola di stato non valida <clause> "</span><span class="sxs-lookup"><span data-stu-id="b8362-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="b8362-166">Errore semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="b8362-167">Per SNMPv1, la clausola STATUS di una chiamata di macro di tipo oggetto deve essere "obbligatoria", "facoltativo", "obsoleto" o "deprecato".</span><span class="sxs-lookup"><span data-stu-id="b8362-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="b8362-168">Per SNMPv2C, la clausola STATUS di una chiamata di macro di tipo oggetto deve essere "Current", "deprecated" o "obsolete".</span><span class="sxs-lookup"><span data-stu-id="b8362-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="b8362-169">Avviso 1004</span><span class="sxs-lookup"><span data-stu-id="b8362-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="b8362-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> : <line \#>: Object-Type <identifier> , la cui sintassi viene risolta in uno dei tipi di contatore non termina con '" della lettera</span><span class="sxs-lookup"><span data-stu-id="b8362-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="b8362-171">Avviso semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="b8362-172">L'identificatore per un oggetto della sintassi del contatore (SNMPv1) o Counter32 e Counter64 (SNMPv2C) deve essere plurale.</span><span class="sxs-lookup"><span data-stu-id="b8362-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="b8362-173">Questo avviso può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b8362-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="b8362-174">Avviso 1005</span><span class="sxs-lookup"><span data-stu-id="b8362-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="b8362-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, avviso>: " <fileName> : <riga \#>: tipo oggetto con sintassi" Sequence of ", deve avere una clausola di accesso" non accessibile "</span><span class="sxs-lookup"><span data-stu-id="b8362-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="b8362-176">Avviso semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="b8362-177">Una tabella o una riga concettuale (rispettivamente, sequenza o tipi di oggetto sequenza) deve essere "non accessibile".</span><span class="sxs-lookup"><span data-stu-id="b8362-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="b8362-178">Questo avviso può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b8362-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="b8362-179">Errore irreversibile 1006</span><span class="sxs-lookup"><span data-stu-id="b8362-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="b8362-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006,> irreversibile: " <fileName> : <riga \#> tipo di oggetto <identifier> , che è di sequenza di sintassi, non ha una clausola index o augments"</span><span class="sxs-lookup"><span data-stu-id="b8362-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="b8362-181">Errore semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="b8362-182">Per SNMPv1, la clausola INDEX deve essere presente per una definizione di tipo oggetto la cui sintassi viene risolta in un tipo di sequenza.</span><span class="sxs-lookup"><span data-stu-id="b8362-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="b8362-183">Per SNMPv2C, è necessario che la clausola INDEX o AUGMENTes sia presente per una dichiarazione di riga concettuale.</span><span class="sxs-lookup"><span data-stu-id="b8362-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="b8362-184">Errore irreversibile 1008</span><span class="sxs-lookup"><span data-stu-id="b8362-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="b8362-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008,> irreversibile: " <fileName> : <riga \#>: il tipo <identifier> di oggetto, che è della sintassi" Sequence ", non è stato fatto riferimento"</span><span class="sxs-lookup"><span data-stu-id="b8362-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="b8362-186">Errore semantico del modulo di chiamata macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8362-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="b8362-187">Un tipo di oggetto con la clausola SYNTAX come tipo di sequenza deve figurare nella clausola della sintassi di una chiamata di tipo oggetto che sta per una dichiarazione di tabella, ovvero un oggetto con la clausola SYNTAX come sequenza di tipo.</span><span class="sxs-lookup"><span data-stu-id="b8362-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="b8362-188">Il parametro <line \#> si riferisce al secondo punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b8362-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="b8362-189">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b8362-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



