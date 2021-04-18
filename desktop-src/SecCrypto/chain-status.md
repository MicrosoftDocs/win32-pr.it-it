---
description: Recupera lo stato di validità della catena o di un certificato specifico nella catena.
title: 'Proprietà IChain2:: status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329347"
---
# <a name="ichain2status-property"></a><span data-ttu-id="bb01a-103">Proprietà IChain2:: status</span><span class="sxs-lookup"><span data-stu-id="bb01a-103">IChain2::Status property</span></span>

<span data-ttu-id="bb01a-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb01a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bb01a-105">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bb01a-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bb01a-106">La proprietà **status** recupera lo stato di validità della catena o di un certificato specifico nella catena.</span><span class="sxs-lookup"><span data-stu-id="bb01a-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb01a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb01a-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="bb01a-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb01a-108">Property value</span></span>

<span data-ttu-id="bb01a-109">Valore **Long** che rappresenta l'indicatore di stato della validità della catena o del certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="bb01a-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="bb01a-110">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="bb01a-110">The following table shows the possible values.</span></span> <span data-ttu-id="bb01a-111">Questa proprietà conterrà zero se la catena o il certificato specificato è valido.</span><span class="sxs-lookup"><span data-stu-id="bb01a-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="bb01a-112">In caso contrario, questa proprietà conterrà una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb01a-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="bb01a-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ L'ATTENDIBILità \_ \_ non è \_ ora \_ valida** (&H00000001)</span><span class="sxs-lookup"><span data-stu-id="bb01a-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-114">Questo certificato o uno dei certificati nella catena di certificati non è ora valido.</span><span class="sxs-lookup"><span data-stu-id="bb01a-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="bb01a-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ L'ATTENDIBILità \_ non è un' \_ \_ ora \_ annidata** (&H00000002)</span><span class="sxs-lookup"><span data-stu-id="bb01a-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-116">I certificati nella catena non sono ora annidati correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb01a-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="bb01a-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ Il TRUST \_ è \_ revocato** (&H00000004)</span><span class="sxs-lookup"><span data-stu-id="bb01a-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-118">La relazione di trust per questo certificato o uno dei certificati nella catena di certificati è stata revocata.</span><span class="sxs-lookup"><span data-stu-id="bb01a-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="bb01a-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ L'ATTENDIBILità \_ \_ non è \_ \_ valida per la firma** (&H00000008)</span><span class="sxs-lookup"><span data-stu-id="bb01a-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-120">Il certificato o uno dei certificati della catena di certificati non dispone di una firma valida.</span><span class="sxs-lookup"><span data-stu-id="bb01a-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="bb01a-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ L'ATTENDIBILità \_ \_ non è \_ valida \_ per l' \_ utilizzo** (&H00000010)</span><span class="sxs-lookup"><span data-stu-id="bb01a-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-122">Il certificato o la catena di certificati non è valida per l'utilizzo proposto.</span><span class="sxs-lookup"><span data-stu-id="bb01a-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="bb01a-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ L'ATTENDIBILità \_ è una \_ \_ radice non attendibile** (&H00000020)</span><span class="sxs-lookup"><span data-stu-id="bb01a-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-124">Il certificato o la catena di certificati si basa su una radice non attendibile.</span><span class="sxs-lookup"><span data-stu-id="bb01a-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="bb01a-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ Stato di revoca ATTENDIBILe \_ \_ \_ sconosciuto** (&H00000040)</span><span class="sxs-lookup"><span data-stu-id="bb01a-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-126">Lo stato di revoca del certificato o di uno dei certificati nella catena di certificati è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bb01a-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="bb01a-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ Il TRUST \_ è \_ ciclico** (&H00000080)</span><span class="sxs-lookup"><span data-stu-id="bb01a-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-128">Uno dei certificati della catena è stato emesso da un' [*autorità di certificazione*](../secgloss/c-gly.md) che il certificato originale certificava.</span><span class="sxs-lookup"><span data-stu-id="bb01a-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="bb01a-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_ \_ Estensione attendibile non valida** (&H00000100)</span><span class="sxs-lookup"><span data-stu-id="bb01a-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-130">Uno dei certificati ha un'estensione non valida.</span><span class="sxs-lookup"><span data-stu-id="bb01a-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="bb01a-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ \_Vincoli di \_ criteri \_ non validi** (&H00000200)</span><span class="sxs-lookup"><span data-stu-id="bb01a-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-132">Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di criteri e uno dei certificati emessi ha un'estensione di mapping dei criteri non consentita o non dispone di un'estensione dei criteri di rilascio richiesta.</span><span class="sxs-lookup"><span data-stu-id="bb01a-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="bb01a-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ ATTENDIBILità \_ \_ \_ vincoli di base non validi** (&H00000400)</span><span class="sxs-lookup"><span data-stu-id="bb01a-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-134">Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di base e il certificato non può essere usato per emettere altri certificati oppure la lunghezza del percorso della catena è stata superata.</span><span class="sxs-lookup"><span data-stu-id="bb01a-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="bb01a-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ \_Vincoli di \_ nome \_ attendibile non validi** (&H00000800)</span><span class="sxs-lookup"><span data-stu-id="bb01a-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-136">Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome non valida.</span><span class="sxs-lookup"><span data-stu-id="bb01a-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="bb01a-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ Il \_ \_ vincolo di \_ \_ nome \_ non è supportato dal trust** (&H00001000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-138">Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome che contiene campi non supportati.</span><span class="sxs-lookup"><span data-stu-id="bb01a-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="bb01a-139">I campi minimo e massimo non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="bb01a-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="bb01a-140">Quindi il valore minimo deve essere sempre zero e il valore massimo deve essere sempre assente.</span><span class="sxs-lookup"><span data-stu-id="bb01a-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="bb01a-141">Per un altro nome è supportato solo UPN.</span><span class="sxs-lookup"><span data-stu-id="bb01a-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="bb01a-142">Le opzioni di nome alternativo seguenti non sono supportate:</span><span class="sxs-lookup"><span data-stu-id="bb01a-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="bb01a-143">Indirizzo X400</span><span class="sxs-lookup"><span data-stu-id="bb01a-143">X400 Address</span></span>
-   <span data-ttu-id="bb01a-144">Nome entità EDI</span><span class="sxs-lookup"><span data-stu-id="bb01a-144">EDI Party Name</span></span>
-   <span data-ttu-id="bb01a-145">ID registrato</span><span class="sxs-lookup"><span data-stu-id="bb01a-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="bb01a-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ \_Vincolo di \_ \_ \_ nome \_ non definito dal trust** (&H00002000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-147">Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome e non è presente un vincolo di nome per una delle opzioni del nome nel certificato finale.</span><span class="sxs-lookup"><span data-stu-id="bb01a-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="bb01a-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ \_ \_ \_ \_ \_ Vincolo Name non consentito** (&H00004000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-149">Il certificato o uno dei certificati nella catena di certificati ha un'estensione di vincoli di nome e non è consentito un vincolo di nome per una delle opzioni del nome nel certificato finale.</span><span class="sxs-lookup"><span data-stu-id="bb01a-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="bb01a-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ Il \_ \_ vincolo di \_ nome \_ è stato escluso dal trust** (&H00008000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-151">Il certificato o uno dei certificati nella catena di certificati ha un'estensione per i vincoli di nome e una delle opzioni relative al nome nel certificato finale viene esclusa in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="bb01a-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="bb01a-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ Il TRUST \_ è la \_ \_ revoca offline** (&H01000000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-153">Lo stato di revoca del certificato o uno dei certificati nella catena di certificati è offline o non aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bb01a-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="bb01a-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ \_Criterio della \_ \_ catena di \_ rilascio non attendibile** (&H02000000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-155">Il certificato finale non ha criteri di rilascio risultanti e uno dei certificati della CA emittente ha un'estensione di vincoli dei criteri che lo richiede.</span><span class="sxs-lookup"><span data-stu-id="bb01a-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="bb01a-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ TRUST \_ è \_ una \_ catena parziale** (&H00010000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-157">La catena di certificati non è competitiva.</span><span class="sxs-lookup"><span data-stu-id="bb01a-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="bb01a-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ Il \_ trust \_ CTL \_ non è \_ ora \_ valido** (&H00020000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-159">Un CTL utilizzato per creare la catena non è tempo valido.</span><span class="sxs-lookup"><span data-stu-id="bb01a-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="bb01a-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ Il \_ trust \_ CTL \_ non \_ è \_ valido per la firma** (&H00040000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-161">Un CTL utilizzato per creare la catena non dispone di una firma valida.</span><span class="sxs-lookup"><span data-stu-id="bb01a-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="bb01a-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ Il \_ trust \_ CTL \_ non è \_ valido \_ per l' \_ utilizzo** (&H00080000)</span><span class="sxs-lookup"><span data-stu-id="bb01a-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="bb01a-163">Un CTL utilizzato per creare la catena non è valido per questo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="bb01a-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb01a-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb01a-164">Requirements</span></span>



| <span data-ttu-id="bb01a-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb01a-165">Requirement</span></span> | <span data-ttu-id="bb01a-166">Valore</span><span class="sxs-lookup"><span data-stu-id="bb01a-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb01a-167">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bb01a-167">End of client support</span></span><br/> | <span data-ttu-id="bb01a-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb01a-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bb01a-169">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bb01a-169">End of server support</span></span><br/> | <span data-ttu-id="bb01a-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb01a-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bb01a-171">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bb01a-171">Redistributable</span></span><br/>       | <span data-ttu-id="bb01a-172">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb01a-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb01a-173">DLL</span><span class="sxs-lookup"><span data-stu-id="bb01a-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bb01a-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb01a-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
