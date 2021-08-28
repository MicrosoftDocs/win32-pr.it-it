---
description: Descrive gli errori del provider SNMP WMI da 231 a 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Errori da 231 a 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f8a6dbbcdd2ab9f7186413b88bf597f1e0a4ca9605fd0a9d8f3eae1d123e97f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131413"
---
# <a name="errors-231-through-240"></a>Errori da 231 a 240

Descrive gli errori del provider SNMP WMI da 231 a 240.

[Errore irreversibile 232](#fatal-error-232)

[Errore irreversibile 233](#fatal-error-233)

[Errore irreversibile 234](#fatal-error-234)

[Errore irreversibile 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Errore irreversibile 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, Errore irreversibile>:" <fileName> :<riga \#>:Chiamata di SNMPv1 OBJECT-TYPE non consentita"**
</dt> <dd>

Errore di sintassi del modulo. È stata usata la chiamata **OBJECT-TYPE** specifica di SNMPv1 nel MIB, ma è stata specificata l'opzione **/v2c,** che richiede una conformità rigorosa alla sintassi SNMPv2C.

</dd> </dl>

## <a name="fatal-error-233"></a>Errore irreversibile 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, Errore irreversibile>: <fileName> ":<line>: Chiamata di \# SNMPv1 SMI TRAP-TYPE non consentita"**
</dt> <dd>

Errore di sintassi del modulo. È stata usata la chiamata **TRAP-TYPE** specifica di SNMPv1 nel MIB, ma è stata specificata l'opzione **/v2c,** che richiede una conformità rigorosa alla sintassi SNMPv2C.

</dd> </dl>

## <a name="fatal-error-234"></a>Errore irreversibile 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, Fatal>:" <fileName> :<line \#>: la chiamata MODULE-IDENTITY è consentita solo immediatamente dopo la sezione IMPORTS"**
</dt> <dd>

Errore di sintassi del modulo. La **chiamata MODULE-IDENTITY** non è stata specificata.

</dd> </dl>

## <a name="fatal-error-236"></a>Errore irreversibile 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236, Fatal>: <fileName> ":<line \#>: Number does not fit into the 32 bit representation used by the compiler"**
</dt> <dd>

Errore di sintassi del modulo nell'assegnazione di valori. Si verifica un errore di assegnazione di valori MIB in cui un valore intero è così grande da richiede più di 32 bit per rappresentarlo.

</dd> </dl>

 

 



