---
description: Descrive gli errori del provider SNMP WMI da 1031 a 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Errori da 1031 a 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315728"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="9e4ee-103">Errori da 1031 a 1040</span><span class="sxs-lookup"><span data-stu-id="9e4ee-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="9e4ee-104">Descrive gli errori del provider SNMP WMI da 1031 a 1040.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="9e4ee-105">Avviso 1031</span><span class="sxs-lookup"><span data-stu-id="9e4ee-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="9e4ee-106">Errore irreversibile 1032</span><span class="sxs-lookup"><span data-stu-id="9e4ee-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="9e4ee-107">Errore irreversibile 1033</span><span class="sxs-lookup"><span data-stu-id="9e4ee-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="9e4ee-108">Avviso 1034</span><span class="sxs-lookup"><span data-stu-id="9e4ee-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="9e4ee-109">Avviso 1036</span><span class="sxs-lookup"><span data-stu-id="9e4ee-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="9e4ee-110">Errore irreversibile 1037</span><span class="sxs-lookup"><span data-stu-id="9e4ee-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="9e4ee-111">Errore irreversibile 1038</span><span class="sxs-lookup"><span data-stu-id="9e4ee-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="9e4ee-112">Errore irreversibile 1039</span><span class="sxs-lookup"><span data-stu-id="9e4ee-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="9e4ee-113">Errore irreversibile 1040</span><span class="sxs-lookup"><span data-stu-id="9e4ee-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="9e4ee-114">Avviso 1031</span><span class="sxs-lookup"><span data-stu-id="9e4ee-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, avviso>: " <fileName> : <riga \#>: <identifier> è necessario importare dal modulo il simbolo standard <identifier> . Presumendo la definizione standard ".**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-116">Avviso semantico del modulo della sezione Imports, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-117">Se un identificatore SNMP noto al compilatore si trova nella sezione Imports, il modulo da cui viene importato deve essere uno dei moduli standard.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="9e4ee-118">Alcune importazioni di uso comune sono "conoscenze presunte" nella parte del compilatore.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="9e4ee-119">Non è necessario che il compilatore richieda l'accesso ad altri moduli di informazioni per risolverli.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="9e4ee-120">Le importazioni SNMPv1 e SNMPv2C predefinite sono descritte nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="9e4ee-121">**Importazioni SNMPv1 predefinite**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="9e4ee-122">Importa classe</span><span class="sxs-lookup"><span data-stu-id="9e4ee-122">Import Class</span></span> | <span data-ttu-id="9e4ee-123">Modulo</span><span class="sxs-lookup"><span data-stu-id="9e4ee-123">Module</span></span>      | <span data-ttu-id="9e4ee-124">Istanze</span><span class="sxs-lookup"><span data-stu-id="9e4ee-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="9e4ee-125">Valore ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9e4ee-125">ASN.1 Value</span></span>  | <span data-ttu-id="9e4ee-126">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="9e4ee-126">RFC1155-SMI</span></span> | <span data-ttu-id="9e4ee-127">Internet, directory, gestione, sperimentale, privato, aziende</span><span class="sxs-lookup"><span data-stu-id="9e4ee-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="9e4ee-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="9e4ee-128">RFC1213-MIB</span></span> | <span data-ttu-id="9e4ee-129">MIB-II e IP, interfacce, trasmissione</span><span class="sxs-lookup"><span data-stu-id="9e4ee-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="9e4ee-130">Tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9e4ee-130">ASN.1 Type</span></span>   | <span data-ttu-id="9e4ee-131">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="9e4ee-131">RFC1155-SMI</span></span> | <span data-ttu-id="9e4ee-132">NetworkAddress, IpAddress, Counter, gauge, TimeTicks, Opaque</span><span class="sxs-lookup"><span data-stu-id="9e4ee-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="9e4ee-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="9e4ee-133">RFC1213-MIB</span></span> | <span data-ttu-id="9e4ee-134">DisplayString, PhysAddress</span><span class="sxs-lookup"><span data-stu-id="9e4ee-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="9e4ee-135">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9e4ee-135">ASN.1 Macro</span></span>  | <span data-ttu-id="9e4ee-136">RFC-1212</span><span class="sxs-lookup"><span data-stu-id="9e4ee-136">RFC-1212</span></span>    | <span data-ttu-id="9e4ee-137">TIPO OGGETTO</span><span class="sxs-lookup"><span data-stu-id="9e4ee-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="9e4ee-138">RFC-1215</span><span class="sxs-lookup"><span data-stu-id="9e4ee-138">RFC-1215</span></span>    | <span data-ttu-id="9e4ee-139">TIPO TRAP</span><span class="sxs-lookup"><span data-stu-id="9e4ee-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="9e4ee-140">**Importazioni SNMPv2C predefinite**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="9e4ee-141">Importa classe</span><span class="sxs-lookup"><span data-stu-id="9e4ee-141">Import Class</span></span>       | <span data-ttu-id="9e4ee-142">Modulo</span><span class="sxs-lookup"><span data-stu-id="9e4ee-142">Module</span></span>      | <span data-ttu-id="9e4ee-143">Istanze</span><span class="sxs-lookup"><span data-stu-id="9e4ee-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e4ee-144">Valore ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9e4ee-144">ASN.1 Value</span></span>        | <span data-ttu-id="9e4ee-145">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="9e4ee-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="9e4ee-146">org, DoD, Internet, directory, MGMT, MIB-2, trasmissione, sperimentale, privato, imprese, sicurezza, SNMPv2, snmpDomains, snmpProxys, snmpModules</span><span class="sxs-lookup"><span data-stu-id="9e4ee-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="9e4ee-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="9e4ee-147">SNMPv2-TM</span></span>   | <span data-ttu-id="9e4ee-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="9e4ee-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="9e4ee-149">Identità dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="9e4ee-149">Object Identity</span></span>    | <span data-ttu-id="9e4ee-150">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="9e4ee-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="9e4ee-151">zeroDotZero</span><span class="sxs-lookup"><span data-stu-id="9e4ee-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="9e4ee-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="9e4ee-152">SNMPv2-TM</span></span>   | <span data-ttu-id="9e4ee-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="9e4ee-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="9e4ee-154">Tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9e4ee-154">ASN.1 Type</span></span>         | <span data-ttu-id="9e4ee-155">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="9e4ee-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="9e4ee-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, gauge32</span><span class="sxs-lookup"><span data-stu-id="9e4ee-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="9e4ee-157">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9e4ee-157">ASN.1 Macro</span></span>        | <span data-ttu-id="9e4ee-158">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="9e4ee-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="9e4ee-159">MODULE-IDENTITY, OGGETTO-IDENTITY, TIPO-OGGETTO, TIPO DI NOTIFICA</span><span class="sxs-lookup"><span data-stu-id="9e4ee-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="9e4ee-160">SNMPv2-CONF</span><span class="sxs-lookup"><span data-stu-id="9e4ee-160">SNMPv2-CONF</span></span> | <span data-ttu-id="9e4ee-161">OGGETTO-GRUPPO, NOTIFICA-GRUPPO, CONFORMITÀ MODULO, AGENTE-FUNZIONALITÀ</span><span class="sxs-lookup"><span data-stu-id="9e4ee-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="9e4ee-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="9e4ee-162">SNMPv2-TC</span></span>   | <span data-ttu-id="9e4ee-163">CONVENZIONE TESTUALE</span><span class="sxs-lookup"><span data-stu-id="9e4ee-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="9e4ee-164">Convenzione testuale</span><span class="sxs-lookup"><span data-stu-id="9e4ee-164">Textual Convention</span></span> | <span data-ttu-id="9e4ee-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="9e4ee-165">SNMPv2-TC</span></span>   | <span data-ttu-id="9e4ee-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, TDomain, Taddress</span><span class="sxs-lookup"><span data-stu-id="9e4ee-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="9e4ee-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="9e4ee-167">SNMPv2-TM</span></span>   | <span data-ttu-id="9e4ee-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="9e4ee-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="9e4ee-169">Errore irreversibile 1032</span><span class="sxs-lookup"><span data-stu-id="9e4ee-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> irreversibile: " <fileName><riga \#>: valore duplicato <value> nell'enumerazione"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-171">Errore semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-172">Non devono essere presenti valori duplicati.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-172">There must not be any duplicate values.</span></span> <span data-ttu-id="9e4ee-173">Il <riga \#> parametro è la posizione della ricorrenza del nome/valore.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="9e4ee-174">Errore irreversibile 1033</span><span class="sxs-lookup"><span data-stu-id="9e4ee-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> irreversibile: " <fileName><riga \#>: nome duplicato <identifier> nell'enumerazione"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-176">Errore semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-177">Non devono essere presenti nomi duplicati.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-177">There must not be any duplicate names.</span></span> <span data-ttu-id="9e4ee-178">Il <riga \#> parametro è la posizione della ricorrenza del nome/valore.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="9e4ee-179">Avviso 1034</span><span class="sxs-lookup"><span data-stu-id="9e4ee-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, avviso>: " <fileName><riga \#>: il valore 0 non è consentito in un'enumerazione"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-181">Avviso semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-182">Si consiglia di non utilizzare un valore denominato zero in un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="9e4ee-183">Avviso 1036</span><span class="sxs-lookup"><span data-stu-id="9e4ee-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, avviso> " <fileName><riga \#>: il valore nell'enumerazione non viene risolto in un numero intero positivo"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-185">Avviso semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-186">In un'enumerazione non è consentito un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="9e4ee-187">Errore irreversibile 1037</span><span class="sxs-lookup"><span data-stu-id="9e4ee-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> irreversibile: " <fileName><riga \#>: l'identificatore <identifier> non viene risolto in una stringa di ottetti o tipi opachi"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-189">Errore semantico del modulo nella specifica di dimensione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-190">Il simbolo usato in una specifica di dimensione deve essere risolto in stringa ottetto o opaco.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="9e4ee-191">Errore irreversibile 1038</span><span class="sxs-lookup"><span data-stu-id="9e4ee-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> irreversibile: " <fileName><riga \#>: l'identificatore non <identifier> risolve un tipo Integer o un tipo di misuratore"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-193">Errore semantico del modulo nella specifica di intervallo.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-193">Module semantic error in range specification.</span></span> <span data-ttu-id="9e4ee-194">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="9e4ee-195">In SNMPv1 il simbolo usato in una specifica di intervallo deve essere risolto in INTEGER o misuratore.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="9e4ee-196">In SNMPv2C il simbolo usato in una specifica di intervallo deve essere risolto in INTEGER, gauge32, Integer32 o Unsigned32.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="9e4ee-197">Errore irreversibile 1039</span><span class="sxs-lookup"><span data-stu-id="9e4ee-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> irreversibile: <fileName><riga \#>: valore negativo utilizzato nella specifica di dimensione "**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-199">Errore semantico del modulo nella specifica di dimensione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-200">Qualsiasi valore utilizzato per specificare le dimensioni non deve essere negativo.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="9e4ee-201">Errore irreversibile 1040</span><span class="sxs-lookup"><span data-stu-id="9e4ee-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="9e4ee-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore nella specifica di dimensione non viene risolto in un valore integrale non negativo"**</span><span class="sxs-lookup"><span data-stu-id="9e4ee-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="9e4ee-203">Errore semantico del modulo nella specifica di intervallo o di dimensione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9e4ee-204">Qualsiasi simbolo utilizzato per specificare un valore in una specifica di dimensione viene risolto in un valore non negativo.</span><span class="sxs-lookup"><span data-stu-id="9e4ee-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



