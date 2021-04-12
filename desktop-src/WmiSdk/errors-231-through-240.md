---
description: Descrive gli errori del provider SNMP WMI da 231 a 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Errori da 231 a 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d053cac57eec9d0055dec56bbfab8304ad3f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233465"
---
# <a name="errors-231-through-240"></a>Errori da 231 a 240

Descrive gli errori del provider SNMP WMI da 231 a 240.

[Errore irreversibile 232](#fatal-error-232)

[Errore irreversibile 233](#fatal-error-233)

[Errore irreversibile 234](#fatal-error-234)

[Errore irreversibile 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Errore irreversibile 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232,> irreversibile: " <fileName> : <riga \#>: chiamata del tipo di oggetto SNMPv1 SMI non consentita"**
</dt> <dd>

Errore di sintassi del modulo. È stata usata la chiamata al **tipo di oggetto** specifico di SNMPv1 nel MIB, ma è stata specificata l'opzione **/V2C** , che richiede una conformità restrittiva alla sintassi di SNMPv2C.

</dd> </dl>

## <a name="fatal-error-233"></a>Errore irreversibile 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233,> irreversibile: " <fileName> : <riga \#>: chiamata del trap-type di SNMPv1 SMI non consentita"**
</dt> <dd>

Errore di sintassi del modulo. In MIB è stata usata la chiamata al **tipo trap** specifico di SNMPv1, ma è stata specificata l'opzione **/V2C** , che richiede una conformità restrittiva alla sintassi SNMPv2C.

</dd> </dl>

## <a name="fatal-error-234"></a>Errore irreversibile 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234,> irreversibile: " <fileName> : <riga \#>: la chiamata all'identità del modulo è consentita solo immediatamente dopo la sezione importazioni"**
</dt> <dd>

Errore di sintassi del modulo. La chiamata di **identità del modulo** non è posizionata.

</dd> </dl>

## <a name="fatal-error-236"></a>Errore irreversibile 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> irreversibile: " <fileName> : <riga \#>: il numero non rientra nella rappresentazione di bit 32 utilizzata dal compilatore"**
</dt> <dd>

Errore di sintassi del modulo nell'assegnazione del valore. Si è verificato un errore di assegnazione del valore MIB in cui un valore integer è talmente grande che richiede più di 32 bit per rappresentarlo.

</dd> </dl>

 

 



