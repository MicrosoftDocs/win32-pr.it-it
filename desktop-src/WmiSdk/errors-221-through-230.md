---
description: Descrive gli errori del provider SNMP WMI da 221 a 230.
ms.assetid: 50ca7a6b-2367-464b-98af-b65b0fab42c4
ms.tgt_platform: multiple
title: Errori da 221 a 230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89dc0fc15d039bca5f1d8740996928b3586fc61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226946"
---
# <a name="errors-221-through-230"></a><span data-ttu-id="daae4-103">Errori da 221 a 230</span><span class="sxs-lookup"><span data-stu-id="daae4-103">Errors 221 through 230</span></span>

<span data-ttu-id="daae4-104">Descrive gli errori del provider SNMP WMI da 221 a 230.</span><span class="sxs-lookup"><span data-stu-id="daae4-104">Describes WMI SNMP provider errors 221 through 230.</span></span>

[<span data-ttu-id="daae4-105">Errore irreversibile 222</span><span class="sxs-lookup"><span data-stu-id="daae4-105">Fatal Error 222</span></span>](#fatal-error-222)

[<span data-ttu-id="daae4-106">Errore irreversibile 223</span><span class="sxs-lookup"><span data-stu-id="daae4-106">Fatal Error 223</span></span>](#fatal-error-223)

[<span data-ttu-id="daae4-107">Errore irreversibile 224</span><span class="sxs-lookup"><span data-stu-id="daae4-107">Fatal Error 224</span></span>](#fatal-error-224)

[<span data-ttu-id="daae4-108">Errore irreversibile 225</span><span class="sxs-lookup"><span data-stu-id="daae4-108">Fatal Error 225</span></span>](#fatal-error-225)

[<span data-ttu-id="daae4-109">Errore irreversibile 226</span><span class="sxs-lookup"><span data-stu-id="daae4-109">Fatal Error 226</span></span>](#fatal-error-226)

[<span data-ttu-id="daae4-110">Errore irreversibile 227</span><span class="sxs-lookup"><span data-stu-id="daae4-110">Fatal Error 227</span></span>](#fatal-error-227)

[<span data-ttu-id="daae4-111">Errore irreversibile 228</span><span class="sxs-lookup"><span data-stu-id="daae4-111">Fatal Error 228</span></span>](#fatal-error-228)

[<span data-ttu-id="daae4-112">Errore irreversibile 229</span><span class="sxs-lookup"><span data-stu-id="daae4-112">Fatal Error 229</span></span>](#fatal-error-229)

[<span data-ttu-id="daae4-113">Avviso 230</span><span class="sxs-lookup"><span data-stu-id="daae4-113">Warning 230</span></span>](#warning-230)

## <a name="fatal-error-222"></a><span data-ttu-id="daae4-114">Errore irreversibile 222</span><span class="sxs-lookup"><span data-stu-id="daae4-114">Fatal Error 222</span></span>

<dl> <dt>

<span data-ttu-id="daae4-115"><span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222,> irreversibile: " <fileName> : <riga \#>: tipo di notifica non consentito in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-115"><span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222, Fatal>: "<fileName>:<line\#>: NOTIFICATION-TYPE not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-116">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-116">Module syntax error.</span></span> <span data-ttu-id="daae4-117">Nel MIB è stato usato il tipo di notifica specifico di SNMPv2C, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-117">You have used the SNMPv2C-specific NOTIFICATION-TYPE in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-223"></a><span data-ttu-id="daae4-118">Errore irreversibile 223</span><span class="sxs-lookup"><span data-stu-id="daae4-118">Fatal Error 223</span></span>

<dl> <dt>

<span data-ttu-id="daae4-119"><span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223,> irreversibile: " <fileName> : <riga \#>: modulo-identità non consentita in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-119"><span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223, Fatal>: "<fileName>:<line\#>: MODULE-IDENTITY not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-120">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-120">Module syntax error.</span></span> <span data-ttu-id="daae4-121">È stata usata l'identità del modulo specifico di SNMPv2C nel MIB, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-121">You have used the SNMPv2C-specific MODULE IDENTITY in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-224"></a><span data-ttu-id="daae4-122">Errore irreversibile 224</span><span class="sxs-lookup"><span data-stu-id="daae4-122">Fatal Error 224</span></span>

<dl> <dt>

<span data-ttu-id="daae4-123"><span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224,> irreversibile: " <fileName> : <riga \#>: oggetto-identità non consentita in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-123"><span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224, Fatal>: "<fileName>:<line\#>: OBJECT-IDENTITY not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-124">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-124">Module syntax error.</span></span> <span data-ttu-id="daae4-125">È stata usata l'identità dell'oggetto specifico di SNMPv2C nel MIB, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-125">You have used the SNMPv2C-specific OBJECT-IDENTITY in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-225"></a><span data-ttu-id="daae4-126">Errore irreversibile 225</span><span class="sxs-lookup"><span data-stu-id="daae4-126">Fatal Error 225</span></span>

<dl> <dt>

<span data-ttu-id="daae4-127"><span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225,> irreversibile: " <fileName> : <riga \#>: la convenzione testuale non è consentita in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-127"><span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225, Fatal>: "<fileName>:<line\#>: TEXTUAL-CONVENTION not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-128">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-128">Module syntax error.</span></span> <span data-ttu-id="daae4-129">È stata usata la convenzione testuale specifica di SNMPv2C nel MIB, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-129">You have used the SNMPv2C-specific TEXTUAL-CONVENTION in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-226"></a><span data-ttu-id="daae4-130">Errore irreversibile 226</span><span class="sxs-lookup"><span data-stu-id="daae4-130">Fatal Error 226</span></span>

<dl> <dt>

<span data-ttu-id="daae4-131"><span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226,> irreversibile: " <fileName> : <riga \#>: oggetto-gruppo non consentito in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-131"><span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226, Fatal>: "<fileName>:<line\#>: OBJECT-GROUP not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-132">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-132">Module syntax error.</span></span> <span data-ttu-id="daae4-133">È stato usato il gruppo di oggetti specifico di SNMPv2C in MIB, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-133">You have used the SNMPv2C-specific OBJECT-GROUP in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-227"></a><span data-ttu-id="daae4-134">Errore irreversibile 227</span><span class="sxs-lookup"><span data-stu-id="daae4-134">Fatal Error 227</span></span>

<dl> <dt>

<span data-ttu-id="daae4-135"><span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227,> irreversibile: " <fileName> : <riga \#>: notifica-gruppo non consentito in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-135"><span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227, Fatal>: "<fileName>:<line\#>: NOTIFICATION-GROUP not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-136">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-136">Module syntax error.</span></span> <span data-ttu-id="daae4-137">È stato usato il gruppo di notifiche specifico di SNMPv2C in MIB, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-137">You have used the SNMPv2C-specific NOTIFICATION-GROUP in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-228"></a><span data-ttu-id="daae4-138">Errore irreversibile 228</span><span class="sxs-lookup"><span data-stu-id="daae4-138">Fatal Error 228</span></span>

<dl> <dt>

<span data-ttu-id="daae4-139"><span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228,> irreversibile: " <fileName> : <riga \#>: conformità del modulo non consentita in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-139"><span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228, Fatal>: "<fileName>:<line\#>: MODULE-COMPLIANCE not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-140">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-140">Module syntax error.</span></span> <span data-ttu-id="daae4-141">È stata usata la conformità del modulo specifica di SNMPv2C nel MIB, ma è stata specificata l'opzione **/V1** , che richiede una rigorosa conformità alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-141">You have used the SNMPv2C-specific MODULE-COMPLIANCE in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-229"></a><span data-ttu-id="daae4-142">Errore irreversibile 229</span><span class="sxs-lookup"><span data-stu-id="daae4-142">Fatal Error 229</span></span>

<dl> <dt>

<span data-ttu-id="daae4-143"><span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229,> irreversibile: " <fileName> : <riga \#>: agente-funzionalità non consentite in SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="daae4-143"><span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229, Fatal>: "<fileName>:<line\#>: AGENT-CAPABILITIES not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-144">Errore di sintassi del modulo.</span><span class="sxs-lookup"><span data-stu-id="daae4-144">Module syntax error.</span></span> <span data-ttu-id="daae4-145">Sono state usate le funzionalità dell'agente specifiche di SNMPv2C nel MIB, ma è stata specificata l'opzione **/V1** , che richiede una conformità restrittiva alla sintassi di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="daae4-145">You have used the SNMPv2C-specific AGENT-CAPABILITIES in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="warning-230"></a><span data-ttu-id="daae4-146">Avviso 230</span><span class="sxs-lookup"><span data-stu-id="daae4-146">Warning 230</span></span>

<dl> <dt>

<span data-ttu-id="daae4-147"><span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, avviso>: " <fileName> : <riga \#>:' <the wrong token> ' utilizzata. Presumendo ':: =' "**</span><span class="sxs-lookup"><span data-stu-id="daae4-147"><span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, Warning>: "<fileName>:<line\#>: '<the wrong token>' used. Assuming '::=' "**</span></span>
</dt> <dd>

<span data-ttu-id="daae4-148">Il token ": =", "::" o "=" è stato usato al posto di ":: =".</span><span class="sxs-lookup"><span data-stu-id="daae4-148">The token ":=", "::", or "=" has been used instead of "::=".</span></span>

</dd> </dl>

 

 



