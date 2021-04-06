---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883274"
---
# <a name="p-security-glossary"></a><span data-ttu-id="0c2c7-103">P (Glossario sulla sicurezza)</span><span class="sxs-lookup"><span data-stu-id="0c2c7-103">P (Security Glossary)</span></span>

<span data-ttu-id="0c2c7-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="0c2c7-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0c2c7-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**imbottitura**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-106">Stringa in genere aggiunta quando l'ultimo blocco di testo non crittografato è breve.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="0c2c7-107">Ad esempio, se la lunghezza del blocco è 64 bit e l'ultimo blocco contiene solo 40 bit, è necessario aggiungere 24 bit di riempimento all'ultimo blocco.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="0c2c7-108">La stringa di riempimento può contenere zeri, zeri alternati o altri criteri.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="0c2c7-109">Le applicazioni che usano [*CryptoAPI*](c-gly.md) non devono aggiungere spaziatura interna al testo non crittografato prima di essere crittografati, né devono essere rimossi dopo la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="0c2c7-110">Questa operazione viene gestita automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro password**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-112">Una DLL che fornisce l'applicazione dei criteri password e la notifica delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="0c2c7-113">Le funzioni implementate dai filtri password vengono chiamate dall' [*autorità di sicurezza locale*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**archiviazione permanente**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-115">Qualsiasi supporto di archiviazione che rimanga intatto quando viene scollegata l'alimentazione.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="0c2c7-116">Molti database dell' [*archivio certificati*](c-gly.md) sono formati di archiviazione permanente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-118">Vedere *standard di crittografia a chiave pubblica*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-120">Gli standard consigliati per l'implementazione della crittografia a chiave pubblica basata sull'algoritmo RSA come definito nella [specifica RFC 3447](https://tools.ietf.org/html/rfc3447).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-122">Lo standard della sintassi scambio informazioni personali, sviluppato e gestito da RSA Data Security, Inc. Questo standard di sintassi specifica un formato portabile per archiviare o trasferire le chiavi private, i certificati e i segreti esterni di un utente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="0c2c7-123">Vedere anche [*certificati*](c-gly.md) e *standard di crittografia a chiave pubblica*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Dati firmati PKCS 7**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-125">Oggetto dati firmato con la chiave pubblica Cryptography Standard \# 7 (PKCS \# 7) e che incapsula le informazioni utilizzate per firmare un file.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="0c2c7-126">In genere include il certificato del firmatario e il [*certificato radice*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-128">Standard della sintassi dei messaggi crittografati.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="0c2c7-129">Si tratta di una sintassi generale per dati crittografabili, come firme digitali e crittografia,</span><span class="sxs-lookup"><span data-stu-id="0c2c7-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="0c2c7-130">Viene inoltre fornita una sintassi per la divulgazione di certificati, elenchi di revoche di certificati e altri attributi del messaggio, ad esempio timestamp, al messaggio.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**\_ \_ Codifica ASN 7 \_ ASN**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-132">[*Tipo di codifica del messaggio*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="0c2c7-133">I tipi di codifica dei messaggi vengono archiviati nella parola più significativa di un valore **DWORD** (il valore è: 0x00010000).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**testo non crittografato**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-135">Messaggio</span><span class="sxs-lookup"><span data-stu-id="0c2c7-135">A message that is not encrypted.</span></span> <span data-ttu-id="0c2c7-136">di testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Immagine PE (Portable Executable)**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-138">Formato eseguibile standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-140">Vedere *funzione pseudo-random*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenziali primarie**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-142">Il \_ pacchetto di autenticazione MsV1 0 definisce un valore stringa Primary Credential Key: la stringa Primary Credentials include le credenziali specificate al momento dell'accesso iniziale.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="0c2c7-143">Include il nome utente e i form con distinzione tra maiuscole e minuscole e con distinzione tra maiuscole e minuscole della password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="0c2c7-144">Vedere anche [*credenziali aggiuntive*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**provider di servizi primario**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-146">Provider di servizi che fornisce le interfacce di controllo alla scheda.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="0c2c7-147">Ogni smart card può registrare il proprio provider di servizi primario nel database delle smart card.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token primario**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-149">Un token di accesso che viene in genere creato solo dal kernel di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="0c2c7-150">Può essere assegnato a un processo per rappresentare le informazioni di sicurezza predefinite per il processo.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="0c2c7-151">Vedere anche [*token di accesso*](a-gly.md) e [*token di rappresentazione*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principale**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-153">Vedere [*entità di sicurezza*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-155">Condizione di isolamento dalla vista o dal segreto.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="0c2c7-156">Per quanto riguarda i messaggi, i messaggi privati sono messaggi crittografati il cui testo è nascosto nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="0c2c7-157">Per quanto riguarda le chiavi, una chiave privata è una chiave segreta nascosta da altri.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**chiave privata**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-159">Metà segreta di una coppia di chiavi utilizzata in un algoritmo a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="0c2c7-160">Le chiavi private vengono in genere utilizzate per crittografare una chiave di sessione simmetrica, includere una firma digitale in un messaggio o decrittografare un messaggio crittografato con la chiave pubblica corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="0c2c7-161">Vedere anche *chiave pubblica*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB della chiave privata**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-163">BLOB della chiave che contiene una coppia di chiavi pubblica/privata completa.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="0c2c7-164">I BLOB di chiavi private vengono utilizzati dai programmi amministrativi per trasportare coppie di chiavi.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="0c2c7-165">Poiché la parte della chiave privata della coppia di chiavi è estremamente riservata, questi BLOB vengono in genere mantenuti crittografati con una crittografia simmetrica.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="0c2c7-166">Questi BLOB di chiavi possono essere usati anche da applicazioni avanzate in cui le coppie di chiavi sono archiviate all'interno dell'applicazione, anziché basarsi sul meccanismo di archiviazione del CSP.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="0c2c7-167">Un BLOB di chiavi viene creato chiamando la funzione **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="0c2c7-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilegio**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-169">Diritto di un utente a eseguire varie operazioni di sistema, come l'arresto del sistema, il caricamento dei driver di periferica o la modifica dell'ora del sistema.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="0c2c7-170">Il token di accesso di un utente contiene un elenco dei privilegi utilizzati dall'utente o dai gruppi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**processo**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-172">Contesto di sicurezza in cui un'applicazione viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-172">The security context under which an application runs.</span></span> <span data-ttu-id="0c2c7-173">In genere, il contesto di sicurezza è associato a un utente, pertanto tutte le applicazioni che sono in esecuzione all'interno di un dato processo ereditano le autorizzazioni e i privilegi dell'utente che le possiede.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROVA \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-175">Vedere *\_ tipo di provider prov DSS*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**\_Tipo di provider prov DSS**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-177">Tipo di provider predefinito che supporta solo firme digitali e hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="0c2c7-178">Specifica l'algoritmo di firma DSA e gli algoritmi di hash MD5 e SHA-1.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROVA \_ DSS \_ DH**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-180">Vedere *tipo di provider di prova \_ DSS \_ DH*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Tipo di \_ provider prov DSS DH**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-182">Tipo di provider predefinito che fornisce gli algoritmi di scambio di chiave, firma digitale e hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="0c2c7-183">È simile al \_ tipo di provider prov DSS.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROVA \_ fortezza**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-185">Vedere *il \_ tipo di provider prova fortezza*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo di provider dimostrativo \_**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-187">Tipo di provider predefinito che fornisce gli algoritmi di scambio di chiave, firma digitale, crittografia e hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="0c2c7-188">I protocolli di crittografia e gli algoritmi specificati da questo tipo di provider sono di proprietà del National Institute of Standards and Technology (NIST).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROVA \_ MS \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-190">Vedere *tipo di provider di prova \_ MS \_ Exchange*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**Tipo di provider di prova \_ MS \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-192">Tipo di provider predefinito progettato per le esigenze di Microsoft Exchange, nonché altre applicazioni compatibili con Microsoft Mail.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="0c2c7-193">Fornisce lo scambio di chiave, la firma digitale, la crittografia e gli algoritmi di hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV \_ RSA \_ completo**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-195">Vedere *\_ tipo di \_ provider completo RSA di prova*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Tipo di \_ provider completo RSA di prova**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-197">Tipo di provider predefinito definito da Microsoft e RSA Data Security, Inc. Questo tipo di provider per utilizzo generico fornisce gli algoritmi di scambio di chiave, firma digitale, crittografia e hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="0c2c7-198">Gli algoritmi di scambio di chiave, firma digitale e crittografia sono basati sulla crittografia a chiave pubblica RSA.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROVA \_ RSA \_ sig**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-200">Vedere *il \_ tipo di provider prov RSA \_ sig*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Tipo di \_ provider prov RSA Sig**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-202">Tipo di provider predefinito definito da Microsoft e dalla sicurezza dei dati RSA.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="0c2c7-203">Questo tipo di provider è un subset di prova \_ RSA \_ full che fornisce solo algoritmi di firma digitale e hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="0c2c7-204">L'algoritmo di firma digitale è un algoritmo di chiave pubblica RSA.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROVA \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-206">Vedere *\_ tipo di provider di prova SSL*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Tipo di provider di prova \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-208">Tipo di provider predefinito che supporta il protocollo Secure Sockets Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="0c2c7-209">Questo tipo fornisce la crittografia chiave, la firma digitale, la crittografia e gli algoritmi di hash.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="0c2c7-210">Una specifica che spiega SSL è disponibile in Netscape Communications Corp.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-212">Vedere [*provider del servizio di crittografia*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**Nome provider**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-214">Nome utilizzato per identificare un CSP.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-214">A name used to identify a CSP.</span></span> <span data-ttu-id="0c2c7-215">Ad esempio, la versione 1,0 del provider di crittografia di base di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="0c2c7-216">Il nome del provider viene in genere utilizzato quando si chiama la funzione **CryptAcquireContext** per la connessione a un CSP.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo di provider**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-218">Termine utilizzato per identificare un tipo di provider del servizio di crittografia (CSP).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="0c2c7-219">I CSP sono raggruppati in tipi di provider diversi che rappresentano famiglie specifiche di protocolli e formati di dati standard.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="0c2c7-220">Diversamente dal nome del provider univoco del CSP, i tipi di provider non sono univoci per un determinato CSP.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="0c2c7-221">Il tipo di provider viene in genere utilizzato quando si chiama la funzione **CryptAcquireContext** per la connessione a un CSP.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**funzione pseudo-random**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-223">PRF Funzione che accetta una chiave, un'etichetta e un valore di inizializzazione come input, quindi produce un output di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**coppia di chiavi pubblica/privata**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-225">Coppia di chiavi di crittografia utilizzata nella crittografia a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="0c2c7-226">Per ogni utente, un CSP gestisce in genere due coppie di chiavi pubbliche/private, ovvero una coppia di chiavi di scambio e una coppia di chiavi di firma digitale.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="0c2c7-227">Entrambe le coppie di chiavi vengono mantenute di sessione in sessione.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="0c2c7-228">Vedere coppia di [*chiavi di scambio*](e-gly.md) e coppia di [*chiavi di firma*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-230">Chiave di crittografia in genere utilizzata per decrittografare una chiave di sessione o una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="0c2c7-231">La chiave pubblica può inoltre essere utilizzata per crittografare un messaggio in modo che possa essere decrittografato soltanto tramite la chiave privata corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="0c2c7-232">Vedere anche *chiave privata*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo a chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-234">Crittografia asimmetrica che utilizza due chiavi, una per la crittografia, la chiave pubblica e l'altra per la decrittografia, la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="0c2c7-235">Come implicito dai nomi delle chiavi, la chiave pubblica usata per codificare il testo non crittografato può essere resa disponibile a chiunque.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="0c2c7-236">Tuttavia, la chiave privata deve rimanere segreta.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-236">However, the private key must remain secret.</span></span> <span data-ttu-id="0c2c7-237">Solo la chiave privata può decrittografare il testo crittografato.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="0c2c7-238">L'algoritmo di chiave pubblica usato in questo processo è lento (nell'ordine di 1.000 volte più lento rispetto agli algoritmi simmetrici) e viene in genere usato per crittografare le chiavi di sessione o per firmare digitalmente un messaggio.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="0c2c7-239">Vedere anche *chiave pubblica* e *chiave privata*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB a chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-241">BLOB utilizzato per archiviare la parte della chiave pubblica di una coppia di chiavi pubblica/privata.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="0c2c7-242">I BLOB di chiave pubblica non vengono crittografati perché la chiave pubblica contenuta in non è segreta.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="0c2c7-243">Un BLOB di chiave pubblica viene creato chiamando la funzione **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="0c2c7-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Standard di crittografia a chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-245">PKCS Set di standard di sintassi per la crittografia a chiave pubblica che copre le funzioni di sicurezza, inclusi i metodi per la firma dei dati, lo scambio di chiavi, la richiesta di certificati, la crittografia e la decrittografia a chiave pubblica e altre funzioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="0c2c7-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**crittografia a chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="0c2c7-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="0c2c7-247">Crittografia basata su una coppia di chiavi, una per crittografare i dati e l'altra per decrittografarli.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="0c2c7-248">Gli algoritmi di crittografia simmetrica utilizzano invece un'unica chiave sia per crittografare sia per decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="0c2c7-249">In pratica, la crittografia a chiave pubblica viene in genere usata per proteggere la chiave di sessione usata da un algoritmo di crittografia simmetrico.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="0c2c7-250">In questo caso, la chiave pubblica viene utilizzata per crittografare la chiave di sessione che a sua volta è stata utilizzata per crittografare i dati, mentre la chiave privata viene utilizzata per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="0c2c7-251">Oltre a proteggere le chiavi di sessione, la crittografia a chiave pubblica può essere utilizzata per includere una firma digitale in un messaggio (tramite la chiave privata) e convalidare tale firma (tramite la chiave pubblica).</span><span class="sxs-lookup"><span data-stu-id="0c2c7-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="0c2c7-252">Vedere anche *algoritmo a chiave pubblica*.</span><span class="sxs-lookup"><span data-stu-id="0c2c7-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 



