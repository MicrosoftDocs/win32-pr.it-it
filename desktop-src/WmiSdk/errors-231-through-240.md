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
# <a name="errors-231-through-240"></a><span data-ttu-id="ace19-103">Errori da 231 a 240</span><span class="sxs-lookup"><span data-stu-id="ace19-103">Errors 231 through 240</span></span>

<span data-ttu-id="ace19-104">Descrive gli errori del provider SNMP WMI da 231 a 240.</span><span class="sxs-lookup"><span data-stu-id="ace19-104">Describes WMI SNMP provider errors 231 through 240.</span></span>

[<span data-ttu-id="ace19-105">Errore irreversibile 232</span><span class="sxs-lookup"><span data-stu-id="ace19-105">Fatal Error 232</span></span>](#fatal-error-232)

[<span data-ttu-id="ace19-106">Errore irreversibile 233</span><span class="sxs-lookup"><span data-stu-id="ace19-106">Fatal Error 233</span></span>](#fatal-error-233)

[<span data-ttu-id="ace19-107">Errore irreversibile 234</span><span class="sxs-lookup"><span data-stu-id="ace19-107">Fatal Error 234</span></span>](#fatal-error-234)

[<span data-ttu-id="ace19-108">Errore irreversibile 236</span><span class="sxs-lookup"><span data-stu-id="ace19-108">Fatal Error 236</span></span>](#fatal-error-236)

## <a name="fatal-error-232"></a><span data-ttu-id="ace19-109">Errore irreversibile 232</span><span class="sxs-lookup"><span data-stu-id="ace19-109">Fatal Error 232</span></span>

<dl> <dt>

<span data-ttu-id="ace19-110"><span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232,> irreversibile: " <fileName> : <riga \#>: chiamata del tipo di oggetto SNMPv1 SMI non consentita"**</span><span class="sxs-lookup"><span data-stu-id="ace19-110"><span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, Fatal>:"<fileName>:<line\#>:Invocation of SNMPv1 SMI OBJECT-TYPE disallowed"**</span></span>
</dt> <dd>

<span data-ttu-id="ace19-111">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="ace19-111">Module syntax error.</span></span> <span data-ttu-id="ace19-112">È stata usata la chiamata al **tipo di oggetto** specifico di SNMPv1 nel MIB, ma è stata specificata l'opzione **/V2C** , che richiede una conformità restrittiva alla sintassi di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ace19-112">You have used the SNMPv1-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v2c** switch, which requires strict conformance to SNMPv2C syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-233"></a><span data-ttu-id="ace19-113">Errore irreversibile 233</span><span class="sxs-lookup"><span data-stu-id="ace19-113">Fatal Error 233</span></span>

<dl> <dt>

<span data-ttu-id="ace19-114"><span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233,> irreversibile: " <fileName> : <riga \#>: chiamata del trap-type di SNMPv1 SMI non consentita"**</span><span class="sxs-lookup"><span data-stu-id="ace19-114"><span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, Fatal>: "<fileName>:<line\#>: Invocation of SNMPv1 SMI TRAP-TYPE disallowed"**</span></span>
</dt> <dd>

<span data-ttu-id="ace19-115">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="ace19-115">Module syntax error.</span></span> <span data-ttu-id="ace19-116">In MIB è stata usata la chiamata al **tipo trap** specifico di SNMPv1, ma è stata specificata l'opzione **/V2C** , che richiede una conformità restrittiva alla sintassi SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ace19-116">You have used the SNMPv1-specific **TRAP-TYPE** invocation in the MIB, but have specified the **/v2c** switch, which requires strict conformance to SNMPv2C syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-234"></a><span data-ttu-id="ace19-117">Errore irreversibile 234</span><span class="sxs-lookup"><span data-stu-id="ace19-117">Fatal Error 234</span></span>

<dl> <dt>

<span data-ttu-id="ace19-118"><span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234,> irreversibile: " <fileName> : <riga \#>: la chiamata all'identità del modulo è consentita solo immediatamente dopo la sezione importazioni"**</span><span class="sxs-lookup"><span data-stu-id="ace19-118"><span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, Fatal>:"<fileName>:<line\#>: MODULE-IDENTITY invocation is allowed only immediately after the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="ace19-119">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="ace19-119">Module syntax error.</span></span> <span data-ttu-id="ace19-120">La chiamata di **identità del modulo** non è posizionata.</span><span class="sxs-lookup"><span data-stu-id="ace19-120">The **MODULE-IDENTITY** invocation is misplaced.</span></span>

</dd> </dl>

## <a name="fatal-error-236"></a><span data-ttu-id="ace19-121">Errore irreversibile 236</span><span class="sxs-lookup"><span data-stu-id="ace19-121">Fatal Error 236</span></span>

<dl> <dt>

<span data-ttu-id="ace19-122"><span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> irreversibile: " <fileName> : <riga \#>: il numero non rientra nella rappresentazione di bit 32 utilizzata dal compilatore"**</span><span class="sxs-lookup"><span data-stu-id="ace19-122"><span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236, Fatal>: "<fileName>:<line\#>: Number does not fit into the 32 bit representation used by the compiler"**</span></span>
</dt> <dd>

<span data-ttu-id="ace19-123">Errore di sintassi del modulo nell'assegnazione del valore.</span><span class="sxs-lookup"><span data-stu-id="ace19-123">Module syntax error in value assignment.</span></span> <span data-ttu-id="ace19-124">Si è verificato un errore di assegnazione del valore MIB in cui un valore integer è talmente grande che richiede più di 32 bit per rappresentarlo.</span><span class="sxs-lookup"><span data-stu-id="ace19-124">There is a MIB value assignment error in which an integer value is so large that it requires more than 32 bits to represent it.</span></span>

</dd> </dl>

 

 



