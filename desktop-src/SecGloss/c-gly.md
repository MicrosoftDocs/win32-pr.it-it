---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: db46def4-bfdc-4801-a57d-d568e94a2dbb
title: C (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863422525326ec0a04a597d33a29553006bb014b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314689"
---
# <a name="c-security-glossary"></a><span data-ttu-id="1c15a-103">C (Glossario sulla sicurezza)</span><span class="sxs-lookup"><span data-stu-id="1c15a-103">C (Security Glossary)</span></span>

<span data-ttu-id="1c15a-104">[A](a-gly.md) [B](b-gly.md) C [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="1c15a-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1c15a-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**CA**</span><span class="sxs-lookup"><span data-stu-id="1c15a-105"><span id="_security_ca_gly"></span><span id="_SECURITY_CA_GLY"></span>**CA**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-106">Vedere *autorità di certificazione*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-106">See *certification authority*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**Certificato CA**</span><span class="sxs-lookup"><span data-stu-id="1c15a-107"><span id="_security_ca_certificate_gly"></span><span id="_SECURITY_CA_CERTIFICATE_GLY"></span>**CA certificate**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-108">Identifica l'autorità di certificazione (CA) che rilascia i certificati di autenticazione server e client ai server e ai client che richiedono tali certificati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-108">Identifies the certification authority (CA) that issues server and client authentication certificates to the servers and clients that request these certificates.</span></span> <span data-ttu-id="1c15a-109">Poiché contiene una chiave pubblica utilizzata nelle firme digitali, tale certificato è anche detto certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="1c15a-109">Because it contains a public key used in digital signatures, it is also referred to as a signature certificate.</span></span> <span data-ttu-id="1c15a-110">Se la CA è un'autorità radice, il certificato della CA può essere definito certificato radice.</span><span class="sxs-lookup"><span data-stu-id="1c15a-110">If the CA is a root authority, the CA certificate may be referred to as a root certificate.</span></span> <span data-ttu-id="1c15a-111">Infine, tale certificato viene talvolta indicato con il termine certificato di sito.</span><span class="sxs-lookup"><span data-stu-id="1c15a-111">Also sometimes known as a site certificate.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**Gerarchia CA**</span><span class="sxs-lookup"><span data-stu-id="1c15a-112"><span id="_security_ca_hierarchy_gly"></span><span id="_SECURITY_CA_HIERARCHY_GLY"></span>**CA hierarchy**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-113">Una gerarchia di autorità di certificazione (CA) contiene più CA.</span><span class="sxs-lookup"><span data-stu-id="1c15a-113">A certification authority (CA) hierarchy contains multiple CAs.</span></span> <span data-ttu-id="1c15a-114">È organizzato in modo tale che ogni autorità di certificazione sia certificata da un'altra autorità di certificazione in un livello superiore della gerarchia fino a quando non viene raggiunta la parte superiore della gerarchia, nota anche come autorità radice.</span><span class="sxs-lookup"><span data-stu-id="1c15a-114">It is organized such that each CA is certified by another CA in a higher level of the hierarchy until the top of the hierarchy, also known as the root authority, is reached.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG \_ DH \_ EPHEM**</span><span class="sxs-lookup"><span data-stu-id="1c15a-115"><span id="_security_calg_dh_ephem_gly"></span><span id="_SECURITY_CALG_DH_EPHEM_GLY"></span>**CALG\_DH\_EPHEM**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-116">Identificatore dell'algoritmo CryptoAPI per l'algoritmo di scambio delle chiavi Diffie-Hellman se usato per la generazione di chiavi temporanee.</span><span class="sxs-lookup"><span data-stu-id="1c15a-116">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of ephemeral keys.</span></span>

<span data-ttu-id="1c15a-117">Vedere anche [*algoritmo di scambio delle chiavi Diffie-Hellman (effimero)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-117">See also [*Diffie-Hellman (ephemeral) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG \_ DH \_ SF**</span><span class="sxs-lookup"><span data-stu-id="1c15a-118"><span id="_security_calg_dh_sf_gly"></span><span id="_SECURITY_CALG_DH_SF_GLY"></span>**CALG\_DH\_SF**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-119">Identificatore dell'algoritmo CryptoAPI per il Diffie-Hellman algoritmo di scambio delle chiavi quando viene utilizzato per la generazione di chiavi di archiviazione e di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="1c15a-119">The CryptoAPI algorithm identifier for the Diffie-Hellman key-exchange algorithm when used for the generation of store-and-forward keys.</span></span>

<span data-ttu-id="1c15a-120">Vedere anche l' [*algoritmo di scambio della chiave Diffie-Hellman (archivia e invia)*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-120">See also [*Diffie-Hellman (store and forward) key-exchange algorithm*](d-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG \_ HMAC**</span><span class="sxs-lookup"><span data-stu-id="1c15a-121"><span id="_security_calg_hmac_gly"></span><span id="_SECURITY_CALG_HMAC_GLY"></span>**CALG\_HMAC**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-122">Identificatore dell'algoritmo CryptoAPI per l'algoritmo di Message Authentication Code basato su hash.</span><span class="sxs-lookup"><span data-stu-id="1c15a-122">The CryptoAPI algorithm identifier for the hash-based Message Authentication Code algorithm.</span></span>

<span data-ttu-id="1c15a-123">Vedere anche [*Message Authentication Code basati su hash*](h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-123">See also [*Hash-Based Message Authentication Code*](h-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**\_Mac CALG**</span><span class="sxs-lookup"><span data-stu-id="1c15a-124"><span id="_security_calg_mac_gly"></span><span id="_SECURITY_CALG_MAC_GLY"></span>**CALG\_MAC**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-125">Identificatore dell'algoritmo CryptoAPI per l'algoritmo Message Authentication Code.</span><span class="sxs-lookup"><span data-stu-id="1c15a-125">The CryptoAPI algorithm identifier for the Message Authentication Code algorithm.</span></span>

<span data-ttu-id="1c15a-126">Vedere anche [*Message Authentication Code*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-126">See also [*Message Authentication Code*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**\_MD2 CALG**</span><span class="sxs-lookup"><span data-stu-id="1c15a-127"><span id="_security_calg_md2_gly"></span><span id="_SECURITY_CALG_MD2_GLY"></span>**CALG\_MD2**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-128">Identificatore dell'algoritmo CryptoAPI per l'algoritmo hash MD2.</span><span class="sxs-lookup"><span data-stu-id="1c15a-128">The CryptoAPI algorithm identifier for the MD2 hash algorithm.</span></span>

<span data-ttu-id="1c15a-129">Vedere anche [*algoritmo MD2*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-129">See also [*MD2 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**\_MD5 CALG**</span><span class="sxs-lookup"><span data-stu-id="1c15a-130"><span id="_security_calg_md5_gly"></span><span id="_SECURITY_CALG_MD5_GLY"></span>**CALG\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-131">Identificatore dell'algoritmo CryptoAPI per l'algoritmo hash MD5.</span><span class="sxs-lookup"><span data-stu-id="1c15a-131">The CryptoAPI algorithm identifier for the MD5 hash algorithm.</span></span>

<span data-ttu-id="1c15a-132">Vedere anche [*algoritmo MD5*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-132">See also [*MD5 algorithm*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="1c15a-133"><span id="_security_calg_rc2_gly"></span><span id="_SECURITY_CALG_RC2_GLY"></span>**CALG\_RC2**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-134">Identificatore dell'algoritmo CryptoAPI per l'algoritmo di crittografia a blocchi RC2.</span><span class="sxs-lookup"><span data-stu-id="1c15a-134">The CryptoAPI algorithm identifier for the RC2 block cipher algorithm.</span></span>

<span data-ttu-id="1c15a-135">Vedere anche [*algoritmo di blocco RC2*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-135">See also [*RC2 block algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="1c15a-136"><span id="_security_calg_rc4_gly"></span><span id="_SECURITY_CALG_RC4_GLY"></span>**CALG\_RC4**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-137">Identificatore dell'algoritmo CryptoAPI per l'algoritmo di crittografia del flusso RC4.</span><span class="sxs-lookup"><span data-stu-id="1c15a-137">The CryptoAPI algorithm identifier for the RC4 stream cipher algorithm.</span></span>

<span data-ttu-id="1c15a-138">Vedere anche [*algoritmo di flusso RC4*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-138">See also [*RC4 stream algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG \_ RSA \_ KEYX**</span><span class="sxs-lookup"><span data-stu-id="1c15a-139"><span id="_security_calg_rsa_keyx_gly"></span><span id="_SECURITY_CALG_RSA_KEYX_GLY"></span>**CALG\_RSA\_KEYX**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-140">Identificatore dell'algoritmo CryptoAPI per l'algoritmo della chiave pubblica RSA se utilizzato per lo scambio di chiave.</span><span class="sxs-lookup"><span data-stu-id="1c15a-140">The CryptoAPI algorithm identifier for the RSA public key algorithm when used for key exchange.</span></span>

<span data-ttu-id="1c15a-141">Vedere anche [*algoritmo di chiave pubblica RSA*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-141">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG \_ - \_ firma RSA**</span><span class="sxs-lookup"><span data-stu-id="1c15a-142"><span id="_security_calg_rsa_sign_gly"></span><span id="_SECURITY_CALG_RSA_SIGN_GLY"></span>**CALG\_RSA\_SIGN**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-143">Identificatore dell'algoritmo CryptoAPI per l'algoritmo della chiave pubblica RSA quando viene usato per generare firme digitali.</span><span class="sxs-lookup"><span data-stu-id="1c15a-143">The CryptoAPI algorithm identifier for the RSA public key algorithm when used to generate digital signatures.</span></span>

<span data-ttu-id="1c15a-144">Vedere anche [*algoritmo di chiave pubblica RSA*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-144">See also [*RSA public key algorithm*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**\_Sha CALG**</span><span class="sxs-lookup"><span data-stu-id="1c15a-145"><span id="_security_calg_sha_gly"></span><span id="_SECURITY_CALG_SHA_GLY"></span>**CALG\_SHA**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-146">Identificatore dell'algoritmo CryptoAPI per l'algoritmo Secure Hash Algorithm (SHA-1).</span><span class="sxs-lookup"><span data-stu-id="1c15a-146">The CryptoAPI algorithm identifier for the Secure Hash Algorithm (SHA-1).</span></span>

<span data-ttu-id="1c15a-147">Vedere anche [*Secure Hash Algorithm*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-147">See also [*Secure Hash Algorithm*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**CAST**</span><span class="sxs-lookup"><span data-stu-id="1c15a-148"><span id="_security_cast_gly"></span><span id="_SECURITY_CAST_GLY"></span>**CAST**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-149">Gruppo di crittografie a blocchi simmetriche di tipo DES sviluppato da C. M.</span><span class="sxs-lookup"><span data-stu-id="1c15a-149">A group of DES-like symmetric block ciphers developed by C. M.</span></span> <span data-ttu-id="1c15a-150">Adams e S. E.</span><span class="sxs-lookup"><span data-stu-id="1c15a-150">Adams and S. E.</span></span> <span data-ttu-id="1c15a-151">Tavares.</span><span class="sxs-lookup"><span data-stu-id="1c15a-151">Tavares.</span></span> <span data-ttu-id="1c15a-152">I \_ tipi di provider prov MS \_ Exchange specificano un particolare algoritmo cast che usa una dimensione di blocco a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="1c15a-152">PROV\_MS\_EXCHANGE provider types specify a particular CAST algorithm that uses a 64-bit block size.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span><span class="sxs-lookup"><span data-stu-id="1c15a-153"><span id="_security_cbc_gly"></span><span id="_SECURITY_CBC_GLY"></span>**CBC**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-154">Vedere *concatenamento di blocchi crittografici*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-154">See *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**certificato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-155"><span id="_security_certificate_gly"></span><span id="_SECURITY_CERTIFICATE_GLY"></span>**certificate**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-156">Attestato dotato di firma digitale contenente informazioni su un'entità e sulla relativa chiave pubblica. Un certificato consente quindi di associare fra loro questi due dati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-156">A digitally signed statement that contains information about an entity and the entity's public key, thus binding these two pieces of information together.</span></span> <span data-ttu-id="1c15a-157">Un certificato viene emesso da un'organizzazione (o da un'entità) attendibile denominata autorità di certificazione (CA) dopo che l' *autorità di certificazione* ha verificato che l'entità è quella che dichiara.</span><span class="sxs-lookup"><span data-stu-id="1c15a-157">A certificate is issued by a trusted organization (or entity) called a *certification authority* (CA) after the CA has verified that the entity is who it says it is.</span></span>

<span data-ttu-id="1c15a-158">I certificati possono contenere vari tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-158">Certificates can contain different types of data.</span></span> <span data-ttu-id="1c15a-159">Ad esempio, un certificato X.509 contiene il formato del certificato, il numero di serie del certificato, l'algoritmo utilizzato per firmare il certificato, il nome della CA che ha rilasciato il certificato, il nome e la chiave pubblica dell'entità che richiede il certificato e la firma della CA.</span><span class="sxs-lookup"><span data-stu-id="1c15a-159">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the CA that issued the certificate, the name and public key of the entity requesting the certificate, and the CA's signature.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**BLOB di certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-160"><span id="_security_certificate_blob_gly"></span><span id="_SECURITY_CERTIFICATE_BLOB_GLY"></span>**certificate BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-161">BLOB che contiene i dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-161">A BLOB that contains the certificate data.</span></span>

<span data-ttu-id="1c15a-162">Un BLOB di certificati viene creato da chiamate a **CryptEncodeObject**.</span><span class="sxs-lookup"><span data-stu-id="1c15a-162">A certificate BLOB is created by calls to **CryptEncodeObject**.</span></span> <span data-ttu-id="1c15a-163">Il processo viene completato quando l'output della chiamata contiene tutti i dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-163">The process is complete when the output of the call contains all the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**contesto del certificato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-164"><span id="_security_certificate_context_gly"></span><span id="_SECURITY_CERTIFICATE_CONTEXT_GLY"></span>**certificate context**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-165">Struttura del \_ contesto del certificato che contiene un handle per un archivio certificati, un puntatore al BLOB del certificato codificato originale, un puntatore a una struttura di informazioni del certificato \_ e un membro del tipo di codifica.</span><span class="sxs-lookup"><span data-stu-id="1c15a-165">A CERT\_CONTEXT structure that contains a handle to a certificate store, a pointer to the original encoded certificate BLOB, a pointer to a CERT\_INFO structure, and an encoding type member.</span></span> <span data-ttu-id="1c15a-166">Si tratta della struttura di **\_ informazioni** del certificato che contiene la maggior parte delle informazioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-166">It is the **CERT\_INFO** structure that contains most of the certificate information.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**funzioni codifica/decodifica certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-167"><span id="_security_certificate_encode_decode_functions_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODE_DECODE_FUNCTIONS_GLY"></span>**certificate encode/decode functions**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-168">Funzioni che gestiscono la conversione di certificati e materiali correlati in formati binari standard che possono essere utilizzati in ambienti diversi.</span><span class="sxs-lookup"><span data-stu-id="1c15a-168">Functions that manage the translation of certificates and related material into standard, binary formats that can be used in different environments.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**tipo di codifica del certificato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-169"><span id="_security_certificate_encoding_type_gly"></span><span id="_SECURITY_CERTIFICATE_ENCODING_TYPE_GLY"></span>**certificate encoding type**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-170">Definisce la modalità di codifica del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-170">Defines how the certificate is encoded.</span></span> <span data-ttu-id="1c15a-171">Il tipo di codifica del certificato viene archiviato nella parola di ordine inferiore della struttura del tipo di codifica (**DWORD**).</span><span class="sxs-lookup"><span data-stu-id="1c15a-171">The certificate encoding type is stored in the low-order word of the encoding type (**DWORD**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Gestione dei certificati su CMS**</span><span class="sxs-lookup"><span data-stu-id="1c15a-172"><span id="_security_certificate_management_over_cms_gly"></span><span id="_SECURITY_CERTIFICATE_MANAGEMENT_OVER_CMS_GLY"></span>**Certificate Management over CMS**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-173">CMC.</span><span class="sxs-lookup"><span data-stu-id="1c15a-173">CMC.</span></span> <span data-ttu-id="1c15a-174">Gestione dei certificati su CMS.</span><span class="sxs-lookup"><span data-stu-id="1c15a-174">Certificate Management over CMS.</span></span> <span data-ttu-id="1c15a-175">CMC è un protocollo di gestione dei certificati che usa la sintassi dei messaggi crittografici (CMS).</span><span class="sxs-lookup"><span data-stu-id="1c15a-175">CMC is a certificate management protocol that uses Cryptographic Message Syntax (CMS).</span></span> <span data-ttu-id="1c15a-176">Microsoft esegue il wrapping delle richieste di certificati CMC in un oggetto richiesta [*PKCS \# 7*](p-gly.md) (CMS) prima di inviare la richiesta a un server di registrazione.</span><span class="sxs-lookup"><span data-stu-id="1c15a-176">Microsoft wraps CMC certificate requests in a [*PKCS \#7*](p-gly.md) (CMS) request object before sending the request to an enrollment server.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**BLOB nome certificato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-177"><span id="_security_certificate_name_blob_gly"></span><span id="_SECURITY_CERTIFICATE_NAME_BLOB_GLY"></span>**certificate name BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-178">Rappresentazione codificata delle informazioni sul nome incluse nei certificati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-178">An encoded representation of the name information that is included in certificates.</span></span> <span data-ttu-id="1c15a-179">Ogni BLOB di nomi viene mappato a una struttura **\_ \_ BLOB del nome del certificato** .</span><span class="sxs-lookup"><span data-stu-id="1c15a-179">Each name BLOB is mapped to a **CERT\_NAME\_BLOB** structure.</span></span>

<span data-ttu-id="1c15a-180">Ad esempio, le informazioni sull'autorità emittente e sull'oggetto a cui fa riferimento una struttura di **\_ informazioni sul certificato** vengono archiviate in due strutture **BLOB del \_ nome \_ del certificato** .</span><span class="sxs-lookup"><span data-stu-id="1c15a-180">For example, the issuer and subject information referenced by a **CERT\_INFO** structure is stored in two **CERT\_NAME\_BLOB** structures.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**criteri dei certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-181"><span id="_security_certificate_policy_gly"></span><span id="_SECURITY_CERTIFICATE_POLICY_GLY"></span>**certificate policy**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-182">Set denominato di regole che indica l'applicabilità dei certificati per una classe specifica di applicazioni con requisiti di sicurezza comuni.</span><span class="sxs-lookup"><span data-stu-id="1c15a-182">A named set of rules that indicate the applicability of certificates for a specific class of applications with common security requirements.</span></span> <span data-ttu-id="1c15a-183">Tali criteri potrebbero, ad esempio, limitare determinati certificati alle transazioni Electronic Data Interchange entro i limiti di prezzo specificati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-183">Such a policy might, for example, limit certain certificates to electronic data interchange transactions within given price limits.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**richiesta di certificato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-184"><span id="_security_certificate_request_gly"></span><span id="_SECURITY_CERTIFICATE_REQUEST_GLY"></span>**certificate request**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-185">Un messaggio elettronico formattato in modo specifico (inviato a una CA) usato per richiedere un certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-185">A specially formatted electronic message (sent to a CA) used to request a certificate.</span></span> <span data-ttu-id="1c15a-186">La richiesta deve contenere le informazioni necessarie per l'autenticazione della richiesta da parte dell'autorità di certificazione, oltre alla chiave pubblica dell'entità che richiede il certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-186">The request must contain the information required by the CA to authenticate the request, plus the public key of the entity requesting the certificate.</span></span>

<span data-ttu-id="1c15a-187">Tutte le informazioni necessarie per creare la richiesta sono mappate a una struttura di **\_ \_ informazioni di richiesta del certificato** .</span><span class="sxs-lookup"><span data-stu-id="1c15a-187">All the information necessary to create the request is mapped to a **CERT\_REQUEST\_INFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**elenco di revoche di certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-188"><span id="_security_certificate_revocation_list_gly"></span><span id="_SECURITY_CERTIFICATE_REVOCATION_LIST_GLY"></span>**certificate revocation list**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-189">CRL Documento gestito e pubblicato da un'autorità di certificazione (CA) che elenca i certificati emessi dalla CA che non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="1c15a-189">(CRL) A document maintained and published by a certification authority (CA) that lists certificates issued by the CA that are no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**server di certificazione**</span><span class="sxs-lookup"><span data-stu-id="1c15a-190"><span id="_security_certificate_server_gly"></span><span id="_SECURITY_CERTIFICATE_SERVER_GLY"></span>**certificate server**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-191">Server che rilascia certificati per una determinata autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="1c15a-191">A server that issues certificates for a particular CA.</span></span> <span data-ttu-id="1c15a-192">Il software del server di certificazione fornisce servizi personalizzabili per l'emissione e la gestione di certificati utilizzati nei sistemi di sicurezza che utilizzano la crittografia a chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="1c15a-192">The certificate server software provides customizable services for issuing and managing certificates used in security systems that employ public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Servizi certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-193"><span id="_security_certificate_services_gly"></span><span id="_SECURITY_CERTIFICATE_SERVICES_GLY"></span>**Certificate Services**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-194">Un servizio software che rilascia certificati per una determinata *autorità di certificazione* (CA).</span><span class="sxs-lookup"><span data-stu-id="1c15a-194">A software service that issues certificates for a particular *certification authority* (CA).</span></span> <span data-ttu-id="1c15a-195">Fornisce servizi personalizzabili per l'emissione e la gestione dei certificati per l'azienda.</span><span class="sxs-lookup"><span data-stu-id="1c15a-195">It provides customizable services for issuing and managing certificates for the enterprise.</span></span> <span data-ttu-id="1c15a-196">I certificati possono essere usati per fornire supporto per l'autenticazione, tra cui posta elettronica sicura, autenticazione basata sul Web e autenticazione con smart card.</span><span class="sxs-lookup"><span data-stu-id="1c15a-196">Certificates can be used to provide authentication support, including secure email, web-based authentication, and smart card authentication.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**Archivio certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-197"><span id="_security_certificate_store_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_GLY"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-198">Un archivio certificati è in genere un archivio permanente in cui vengono memorizzati i certificati, gli elenchi di revoche di certificati (CRL, Certificate Revocation List) e gli elenchi di certificati attendibili (CTL, Certificate Trust List).</span><span class="sxs-lookup"><span data-stu-id="1c15a-198">Typically, a permanent storage where certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs) are stored.</span></span> <span data-ttu-id="1c15a-199">Quando si utilizzano certificati che non richiedono un'archiviazione permanente è tuttavia possibile creare e aprire un archivio certificati che risiede soltanto in memoria.</span><span class="sxs-lookup"><span data-stu-id="1c15a-199">It is possible, however, to create and open a certificate store solely in memory when working with certificates that do not need to be put in permanent storage.</span></span>

<span data-ttu-id="1c15a-200">L'archivio certificati è fondamentale per la maggior parte delle funzionalità dei certificati in CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="1c15a-200">The certificate store is central to much of the certificate functionality in CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**funzioni dell'archivio certificati**</span><span class="sxs-lookup"><span data-stu-id="1c15a-201"><span id="_security_certificate_store_functions_gly"></span><span id="_SECURITY_CERTIFICATE_STORE_FUNCTIONS_GLY"></span>**certificate store functions**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-202">Funzioni che gestiscono i dati di archiviazione e recupero, ad esempio certificati, elenchi di revoche di certificati (CRL) ed elenchi di certificati attendibili (scopi consentiti).</span><span class="sxs-lookup"><span data-stu-id="1c15a-202">Functions that manage the storage and retrieval data such as certificates, certificate revocation lists (CRLs), and certificate trust lists (CTLs).</span></span> <span data-ttu-id="1c15a-203">Queste funzioni possono essere separate in funzioni di certificato comuni, funzioni elenco di revoche di certificati e funzioni elenco certificati attendibili.</span><span class="sxs-lookup"><span data-stu-id="1c15a-203">These functions can be separated into common certificate functions, certificate revocation list functions, and certificate trust list functions.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**modello di certificato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-204"><span id="_security_certificate_template_gly"></span><span id="_SECURITY_CERTIFICATE_TEMPLATE_GLY"></span>**certificate template**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-205">Costrutto di Windows che consente di profilare certificati, ovvero prespecificando il formato e il contenuto, in base all'utilizzo previsto.</span><span class="sxs-lookup"><span data-stu-id="1c15a-205">A Windows construct that profiles certificates (that is, it prespecifies the format and content) based on their intended usage.</span></span> <span data-ttu-id="1c15a-206">Quando si richiede un [*certificato*](/windows) da un'autorità di *certificazione* dell'organizzazione (Enterprise) di Windows, i richiedenti di certificati sono, a seconda dei rispettivi diritti di accesso, in grado di effettuare una selezione da un'ampia gamma di tipi di certificati basati su modelli di certificato, ad esempio la firma del codice e dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1c15a-206">When requesting a [*certificate*](/windows) from a Windows enterprise *certification authority* (CA), certificate requesters are, depending on their access rights, able to select from a variety of certificate types that are based on certificate templates, such as User and Code Signing.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**elenco certificati attendibili**</span><span class="sxs-lookup"><span data-stu-id="1c15a-207"><span id="_security_certificate_trust_list_gly"></span><span id="_SECURITY_CERTIFICATE_TRUST_LIST_GLY"></span>**certificate trust list**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-208">CTL Elenco predefinito di elementi firmati da un'entità attendibile.</span><span class="sxs-lookup"><span data-stu-id="1c15a-208">(CTL) A predefined list of items that have been signed by a trusted entity.</span></span> <span data-ttu-id="1c15a-209">Un CTL può presentarsi in varie forme, ad esempio un elenco di hash di certificati o un elenco di nomi di file.</span><span class="sxs-lookup"><span data-stu-id="1c15a-209">A CTL can be anything, such as a list of hashes of certificates, or a list of file names.</span></span> <span data-ttu-id="1c15a-210">Tutti gli elementi dell'elenco sono autenticati (ovvero approvati) dall'entità che li ha firmati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-210">All the items in the list are authenticated (approved) by the signing entity.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**autorità di certificazione**</span><span class="sxs-lookup"><span data-stu-id="1c15a-211"><span id="_security_certification_authority_gly"></span><span id="_SECURITY_CERTIFICATION_AUTHORITY_GLY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-212">CA Entità considerata attendibile per emettere certificati che asseriscono che l'utente, il computer o l'organizzazione che ha richiesto il certificato soddisfi le condizioni di un criterio stabilito.</span><span class="sxs-lookup"><span data-stu-id="1c15a-212">(CA) An entity entrusted to issue certificates that assert that the recipient individual, computer, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span><span class="sxs-lookup"><span data-stu-id="1c15a-213"><span id="_security_cfb_gly"></span><span id="_SECURITY_CFB_GLY"></span>**CFB**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-214">Vedere *feedback crittografico*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-214">See *Cipher Feedback*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**modalità di concatenamento**</span><span class="sxs-lookup"><span data-stu-id="1c15a-215"><span id="_security_chaining_mode_gly"></span><span id="_SECURITY_CHAINING_MODE_GLY"></span>**chaining mode**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-216">Modalità di crittografia a blocchi che introduce il feedback combinando testo crittografato e testo normale.</span><span class="sxs-lookup"><span data-stu-id="1c15a-216">A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="1c15a-217">Vedere anche *concatenamento di blocchi crittografici*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-217">See also *Cipher Block Chaining*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-218"><span id="_security_cipher_gly"></span><span id="_SECURITY_CIPHER_GLY"></span>**cipher**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-219">Algoritmo di crittografia utilizzato per crittografare i dati. ovvero per trasformare il testo non crittografato in testo crittografato usando una chiave predefinita.</span><span class="sxs-lookup"><span data-stu-id="1c15a-219">A cryptographic algorithm used to encrypt data; that is, to transform plaintext into ciphertext using a predefined key.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Concatenamento di blocchi crittografici**</span><span class="sxs-lookup"><span data-stu-id="1c15a-220"><span id="_security_cipher_block_chaining_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_GLY"></span>**Cipher Block Chaining**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-221">CBC Metodo di gestione di una crittografia a blocchi simmetrica che usa il feedback per combinare il testo crittografato generato in precedenza con un nuovo testo normale.</span><span class="sxs-lookup"><span data-stu-id="1c15a-221">(CBC) A method of operating a symmetric block cipher that uses feedback to combine previously generated ciphertext with new plaintext.</span></span>

<span data-ttu-id="1c15a-222">Ogni blocco di testo normale viene combinato con il testo crittografato del blocco precedente mediante un'operazione **Xor** bit per bit prima della crittografia.</span><span class="sxs-lookup"><span data-stu-id="1c15a-222">Each plaintext block is combined with the ciphertext of the previous block by a bitwise-**XOR** operation before it is encrypted.</span></span> <span data-ttu-id="1c15a-223">Combinando testo crittografato e testo normale si garantisce che anche se il testo non crittografato contiene molti blocchi identici, ognuno di essi viene crittografato in un blocco crittografato diverso</span><span class="sxs-lookup"><span data-stu-id="1c15a-223">Combining ciphertext and plaintext ensures that even if the plaintext contains many identical blocks, they will each encrypt to a different ciphertext block.</span></span>

<span data-ttu-id="1c15a-224">Quando si utilizza il provider di crittografia di base Microsoft, CBC è la modalità di crittografia predefinita.</span><span class="sxs-lookup"><span data-stu-id="1c15a-224">When the Microsoft Base Cryptographic Provider is used, CBC is the default cipher mode.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**MAC con concatenamento di blocchi crittografici**</span><span class="sxs-lookup"><span data-stu-id="1c15a-225"><span id="_security_cipher_block_chaining_mac_gly"></span><span id="_SECURITY_CIPHER_BLOCK_CHAINING_MAC_GLY"></span>**Cipher Block Chaining MAC**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-226">Metodo di crittografia a blocchi che esegue la crittografia dei dati di base con una crittografia a blocchi, quindi utilizza l'ultimo blocco crittografato come valore hash.</span><span class="sxs-lookup"><span data-stu-id="1c15a-226">A block cipher method that encrypts the base data with a block cipher and then uses the last encrypted block as the hash value.</span></span> <span data-ttu-id="1c15a-227">L'algoritmo di crittografia utilizzato per compilare il [*Message Authentication Code*](m-gly.md) (Mac) è quello specificato al momento della creazione della chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="1c15a-227">The encryption algorithm used to build the [*Message Authentication Code*](m-gly.md) (MAC) is the one that was specified when the session key was created.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Commenti e suggerimenti di crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-228"><span id="_security_cipher_feedback_gly"></span><span id="_SECURITY_CIPHER_FEEDBACK_GLY"></span>**Cipher Feedback**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-229">CFB Modalità di crittografia a blocchi che elabora piccoli incrementi di testo non crittografato in testo crittografato, anziché elaborare un intero blocco alla volta.</span><span class="sxs-lookup"><span data-stu-id="1c15a-229">(CFB) A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="1c15a-230">Questa modalità utilizza un registro di spostamento che è una dimensione del blocco di lunghezza e divisa in sezioni.</span><span class="sxs-lookup"><span data-stu-id="1c15a-230">This mode uses a shift register that is one block size in length and divided into sections.</span></span> <span data-ttu-id="1c15a-231">Se, ad esempio, la dimensione del blocco è 64 bit con otto bit elaborati alla volta, il registro di spostamento viene diviso in otto sezioni.</span><span class="sxs-lookup"><span data-stu-id="1c15a-231">For example, if the block size is 64 bits with eight bits processed at a time, then the shift register would be divided into eight sections.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**modalità di crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-232"><span id="_security_cipher_mode_gly"></span><span id="_SECURITY_CIPHER_MODE_GLY"></span>**cipher mode**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-233">Una modalità di crittografia a blocchi (ogni blocco viene crittografata singolarmente) che può essere specificata tramite la funzione **CryptSetKeyParam** .</span><span class="sxs-lookup"><span data-stu-id="1c15a-233">A block cipher mode (each block is encrypted individually) that can be specified by using the **CryptSetKeyParam** function.</span></span> <span data-ttu-id="1c15a-234">Se l'applicazione non specifica in modo esplicito una di queste modalità, viene utilizzata la modalità di crittografia CBC (Cipher Block Chaining).</span><span class="sxs-lookup"><span data-stu-id="1c15a-234">If the application does not explicitly specify one of these modes, then the cipher block chaining (CBC) cipher mode is used.</span></span>

<span data-ttu-id="1c15a-235">BCE: modalità di crittografia A blocchi che non usa commenti.</span><span class="sxs-lookup"><span data-stu-id="1c15a-235">ECB: A block cipher mode that uses no feedback.</span></span>

<span data-ttu-id="1c15a-236">CBC: modalità di crittografia A blocchi che introduce il feedback combinando testo crittografato e testo normale.</span><span class="sxs-lookup"><span data-stu-id="1c15a-236">CBC: A block cipher mode that introduces feedback by combining ciphertext and plaintext.</span></span>

<span data-ttu-id="1c15a-237">CFB: modalità di crittografia a blocchi che elabora piccoli incrementi di testo non crittografato in testo crittografato, anziché elaborare un intero blocco alla volta.</span><span class="sxs-lookup"><span data-stu-id="1c15a-237">CFB: A block cipher mode that processes small increments of plaintext into ciphertext, instead of processing an entire block at a time.</span></span>

<span data-ttu-id="1c15a-238">OFB: modalità di crittografia a blocchi che usa feedback simile a CFB.</span><span class="sxs-lookup"><span data-stu-id="1c15a-238">OFB: A block cipher mode that uses feedback similar to CFB.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**ciphertext**</span><span class="sxs-lookup"><span data-stu-id="1c15a-239"><span id="_security_ciphertext_gly"></span><span id="_SECURITY_CIPHERTEXT_GLY"></span>**ciphertext**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-240">Messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-240">A message that has been encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**testo non crittografato**</span><span class="sxs-lookup"><span data-stu-id="1c15a-241"><span id="_security_cleartext_gly"></span><span id="_SECURITY_CLEARTEXT_GLY"></span>**cleartext**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-242">Vedere [*testo non crittografato*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-242">See [*plaintext*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**client**</span><span class="sxs-lookup"><span data-stu-id="1c15a-243"><span id="_security_client_gly"></span><span id="_SECURITY_CLIENT_GLY"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-244">L'applicazione, anziché l'applicazione server, che avvia una connessione a un server.</span><span class="sxs-lookup"><span data-stu-id="1c15a-244">The application, rather than the server application, that initiates a connection to a server.</span></span>

<span data-ttu-id="1c15a-245">Confronta con [*Server*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1c15a-245">Compare with [*server*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**certificato client**</span><span class="sxs-lookup"><span data-stu-id="1c15a-246"><span id="_security_client_certificate_gly"></span><span id="_SECURITY_CLIENT_CERTIFICATE_GLY"></span>**client certificate**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-247">Fa riferimento a un certificato utilizzato per l'autenticazione client, ad esempio l'autenticazione di un Web browser in un server Web.</span><span class="sxs-lookup"><span data-stu-id="1c15a-247">Refers to a certificate used for client authentication, such as authenticating a web browser on a web server.</span></span> <span data-ttu-id="1c15a-248">Quando un client del browser Web tenta di accedere a un server Web protetto, il client invia il certificato al server per consentire la verifica dell'identità del client.</span><span class="sxs-lookup"><span data-stu-id="1c15a-248">When a web browser client attempts to access a secured web server, the client sends its certificate to the server to allow it to verify the client's identity.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span><span class="sxs-lookup"><span data-stu-id="1c15a-249"><span id="_security_cmc_gly"></span><span id="_SECURITY_CMC_GLY"></span>**CMC**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-250">Vedere *Gestione certificati su CMS*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-250">See *Certificate Management over CMS*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span><span class="sxs-lookup"><span data-stu-id="1c15a-251"><span id="_security_cng_gly"></span><span id="_SECURITY_CNG_GLY"></span>**CNG**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-252">Vedere *Cryptography API: Next Generation*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-252">See *Cryptography API: Next Generation*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**protocollo di comunicazione**</span><span class="sxs-lookup"><span data-stu-id="1c15a-253"><span id="_security_communication_protocol_gly"></span><span id="_SECURITY_COMMUNICATION_PROTOCOL_GLY"></span>**communication protocol**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-254">Metodo in cui i dati vengono serializzati (convertiti in una stringa di uno e zero) e deserializzati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-254">The method in which data is serialized (converted to a string of ones and zeros) and deserialized.</span></span> <span data-ttu-id="1c15a-255">Il protocollo è controllato sia dal software che dall'hardware per la trasmissione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-255">The protocol is controlled by both software and data-transmission hardware.</span></span>

<span data-ttu-id="1c15a-256">In genere illustrato in termini di livelli, un protocollo di comunicazione semplificato potrebbe essere costituito da un livello dell'applicazione, da un livello di codifica/decodifica e da un livello hardware.</span><span class="sxs-lookup"><span data-stu-id="1c15a-256">Typically discussed in terms of layers, a simplified communication protocol might consist of an application layer, encode/decode layer, and hardware layer.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**delega vincolata**</span><span class="sxs-lookup"><span data-stu-id="1c15a-257"><span id="_security_constrained_delegation_gly"></span><span id="_SECURITY_CONSTRAINED_DELEGATION_GLY"></span>**constrained delegation**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-258">Comportamento che consente al server di inviare richieste per conto del client solo a un elenco di servizi specificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-258">Behavior that allows the server to forward requests on behalf of the client only to a specified list of services.</span></span>

<span data-ttu-id="1c15a-259">**Windows XP:** La delega vincolata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="1c15a-259">**Windows XP:** Constrained delegation is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**contesto**</span><span class="sxs-lookup"><span data-stu-id="1c15a-260"><span id="_security_context_gly"></span><span id="_SECURITY_CONTEXT_GLY"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-261">Dati di sicurezza relativi a una connessione.</span><span class="sxs-lookup"><span data-stu-id="1c15a-261">The security data relevant to a connection.</span></span> <span data-ttu-id="1c15a-262">Un contesto contiene informazioni quali una chiave di sessione e la durata della sessione.</span><span class="sxs-lookup"><span data-stu-id="1c15a-262">A context contains information such as a session key and duration of the session.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**funzione context**</span><span class="sxs-lookup"><span data-stu-id="1c15a-263"><span id="_security_context_function_gly"></span><span id="_SECURITY_CONTEXT_FUNCTION_GLY"></span>**context function**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-264">Funzioni utilizzate per la connessione a un provider del servizio di crittografia (CSP).</span><span class="sxs-lookup"><span data-stu-id="1c15a-264">Functions used to connect to a cryptographic service provider (CSP).</span></span> <span data-ttu-id="1c15a-265">Queste funzioni consentono alle applicazioni di scegliere un CSP specifico per nome o di ottenerne uno con una classe di funzionalità necessaria.</span><span class="sxs-lookup"><span data-stu-id="1c15a-265">These functions enable applications to choose a specific CSP by name or get one with a needed class of functionality.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**controfirma**</span><span class="sxs-lookup"><span data-stu-id="1c15a-266"><span id="_security_countersignature_gly"></span><span id="_SECURITY_COUNTERSIGNATURE_GLY"></span>**countersignature**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-267">Firma di una firma esistente e di un messaggio o firma di una firma esistente.</span><span class="sxs-lookup"><span data-stu-id="1c15a-267">A signature of an existing signature and message or a signature of an existing signature.</span></span> <span data-ttu-id="1c15a-268">Un controfirma viene usato per firmare l'hash crittografato di una firma esistente o per contrassegnare il timestamp di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="1c15a-268">A countersignature is used to sign the encrypted hash of an existing signature or to time stamp a message.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**credenziali**</span><span class="sxs-lookup"><span data-stu-id="1c15a-269"><span id="_security_credentials_gly"></span><span id="_SECURITY_CREDENTIALS_GLY"></span>**credentials**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-270">I dati di accesso autenticati in precedenza usati da un' [*entità di sicurezza*](s-gly.md) per stabilire la propria identità, ad esempio una password o un ticket del protocollo Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1c15a-270">Previously authenticated logon data used by a [*security principal*](s-gly.md) to establish its own identity, such as a password, or a Kerberos protocol ticket.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span><span class="sxs-lookup"><span data-stu-id="1c15a-271"><span id="_security_crl_gly"></span><span id="_SECURITY_CRL_GLY"></span>**CRL**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-272">Vedere l' *elenco di revoche di certificati*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-272">See *certificate revocation list*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**\_codifica ASN di Crypt \_**</span><span class="sxs-lookup"><span data-stu-id="1c15a-273"><span id="_security_crypt_asn_encoding_gly"></span><span id="_SECURITY_CRYPT_ASN_ENCODING_GLY"></span>**CRYPT\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-274">Tipo di codifica che specifica la codifica del certificato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-274">Encoding type that specifies certificate encoding.</span></span> <span data-ttu-id="1c15a-275">I tipi di codifica del certificato vengono archiviati nella parola di ordine inferiore di un valore **DWORD** (il valore è: 0x00000001).</span><span class="sxs-lookup"><span data-stu-id="1c15a-275">Certificate encoding types are stored in the low-order word of a **DWORD** (value is: 0x00000001).</span></span> <span data-ttu-id="1c15a-276">Questo tipo di codifica è funzionalmente identico al tipo di \_ codifica X509 ASN \_ Encoding.</span><span class="sxs-lookup"><span data-stu-id="1c15a-276">This encoding type is functionally the same as the X509\_ASN\_ENCODING encoding type.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**crittanalisi**</span><span class="sxs-lookup"><span data-stu-id="1c15a-277"><span id="_security_cryptoanalysis_gly"></span><span id="_SECURITY_CRYPTOANALYSIS_GLY"></span>**cryptanalysis**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-278">La crittanalisi è l'arte e la scienza della suddivisione del testo crittografato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-278">Cryptanalysis is the art and science of breaking ciphertext.</span></span> <span data-ttu-id="1c15a-279">Al contrario, l'arte e la scienza del mantenimento dei messaggi protetti sono la crittografia.</span><span class="sxs-lookup"><span data-stu-id="1c15a-279">In contrast, the art and science of keeping messages secure is cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span><span class="sxs-lookup"><span data-stu-id="1c15a-280"><span id="_security_cryptoapi_gly"></span><span id="_SECURITY_CRYPTOAPI_GLY"></span>**CryptoAPI**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-281">Interfaccia di programmazione dell'applicazione che consente agli sviluppatori di applicazioni di aggiungere autenticazione, codifica e crittografia alle applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="1c15a-281">Application programming interface that enables application developers to add authentication, encoding, and encryption to Windows-based applications.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**algoritmo di crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-282"><span id="_security_cryptographic_algorithm_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_ALGORITHM_GLY"></span>**cryptographic algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-283">Funzione matematica utilizzata per la crittografia e la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="1c15a-283">A mathematical function used for encryption and decryption.</span></span> <span data-ttu-id="1c15a-284">La maggior parte degli algoritmi di crittografia si basa su una crittografia di sostituzione, una crittografia di trasposizione o una combinazione di entrambi.</span><span class="sxs-lookup"><span data-stu-id="1c15a-284">Most cryptographic algorithms are based on a substitution cipher, a transposition cipher, or a combination of both.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Digest crittografico**</span><span class="sxs-lookup"><span data-stu-id="1c15a-285"><span id="_security_cryptographic_digest_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_DIGEST_GLY"></span>**Cryptographic Digest**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-286">Funzione hash unidirezionale che accetta una stringa di input a lunghezza variabile e la converte in una stringa di output a lunghezza fissa, denominata digest crittografico. Questa stringa di output a lunghezza fissa è probabilisticamente univoca per ogni stringa di input diversa e pertanto può fungere da impronta digitale di un file.</span><span class="sxs-lookup"><span data-stu-id="1c15a-286">A one-way hash function that takes a variable-length input string and converts it to a fixed-length output string (called a cryptographic digest.) This fixed-length output string is probabilistically unique for every different input string and thus can act as a fingerprint of a file.</span></span> <span data-ttu-id="1c15a-287">Quando viene scaricato un file con un digest crittografico, il ricevitore ricalcola il digest.</span><span class="sxs-lookup"><span data-stu-id="1c15a-287">When a file with a cryptographic digest is downloaded, the receiver recomputes the digest.</span></span> <span data-ttu-id="1c15a-288">Se la stringa di output corrisponde al digest contenuto nel file, il destinatario ha la prova che il file ricevuto non è stato manomesso ed è identico al file originariamente inviato.</span><span class="sxs-lookup"><span data-stu-id="1c15a-288">If the output string matches the digest contained in the file, the receiver has proof that the received file was not tampered with and is identical to the file originally sent.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**chiave crittografica**</span><span class="sxs-lookup"><span data-stu-id="1c15a-289"><span id="_security_cryptographic_key_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_KEY_GLY"></span>**cryptographic key**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-290">Una chiave crittografica è una porzione di dati necessaria per inizializzare un algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1c15a-290">A cryptographic key is a piece of data that is required to initialize a cryptographic algorithm.</span></span> <span data-ttu-id="1c15a-291">I sistemi crittografici sono in genere progettati in modo che la loro sicurezza dipenda solo dalla sicurezza delle chiavi crittografiche e non, ad esempio, per mantenere il segreto degli algoritmi.</span><span class="sxs-lookup"><span data-stu-id="1c15a-291">Cryptographic systems are generally designed so that their security depends only on the security of their cryptographic keys and not, for example, on keeping their algorithms secret.</span></span>

<span data-ttu-id="1c15a-292">Esistono molti tipi diversi di chiavi crittografiche, corrispondenti all'ampia gamma di algoritmi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1c15a-292">There are many different types of cryptographic keys, corresponding to the wide variety of cryptographic algorithms.</span></span> <span data-ttu-id="1c15a-293">Le chiavi possono essere classificate in base al tipo di algoritmo utilizzato con, ad esempio come chiavi simmetriche o asimmetriche.</span><span class="sxs-lookup"><span data-stu-id="1c15a-293">Keys can be classified according to the type of algorithm they are used with (for example, as symmetric or asymmetric keys).</span></span> <span data-ttu-id="1c15a-294">Possono anche essere classificati in base alla loro durata in un sistema, ad esempio le chiavi di sessione o di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="1c15a-294">They can also be classified based on their lifetime within a system (for example, as long-lived or session keys).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**provider del servizio di crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-295"><span id="_security_cryptographic_service_provider_gly"></span><span id="_SECURITY_CRYPTOGRAPHIC_SERVICE_PROVIDER_GLY"></span>**cryptographic service provider**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-296">CSP Un modulo software indipendente che esegue effettivamente algoritmi di crittografia per l'autenticazione, la codifica e la crittografia.</span><span class="sxs-lookup"><span data-stu-id="1c15a-296">(CSP) An independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**Cryptography**</span><span class="sxs-lookup"><span data-stu-id="1c15a-297"><span id="_security_cryptography_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_GLY"></span>**cryptography**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-298">L'arte e la scienza della sicurezza delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="1c15a-298">The art and science of information security.</span></span> <span data-ttu-id="1c15a-299">Sono inclusi la riservatezza delle informazioni, l'integrità dei dati, l'autenticazione dell'entità e l'autenticazione dell'origine dati.</span><span class="sxs-lookup"><span data-stu-id="1c15a-299">It includes information confidentiality, data integrity, entity authentication, and data origin authentication.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**API di crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-300"><span id="_security_cryptography_api_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API_GLY"></span>**Cryptography API**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-301">Vedere *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-301">See *CryptoAPI*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**API di crittografia: prossima generazione**</span><span class="sxs-lookup"><span data-stu-id="1c15a-302"><span id="_security_cryptography_api__next_generation_gly"></span><span id="_SECURITY_CRYPTOGRAPHY_API__NEXT_GENERATION_GLY"></span>**Cryptography API: Next Generation**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-303">CNG Seconda generazione della *CryptoAPI*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-303">(CNG) The second generation of the *CryptoAPI*.</span></span> <span data-ttu-id="1c15a-304">CNG consente di sostituire i provider di algoritmi esistenti con i propri provider e aggiungere nuovi algoritmi Man mano che diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="1c15a-304">CNG allows you to replace existing algorithm providers with your own providers and add new algorithms as they become available.</span></span> <span data-ttu-id="1c15a-305">CNG consente inoltre di utilizzare le stesse API da applicazioni in modalità utente e kernel.</span><span class="sxs-lookup"><span data-stu-id="1c15a-305">CNG also allows the same APIs to be used from user and kernel mode applications.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**crittografia**</span><span class="sxs-lookup"><span data-stu-id="1c15a-306"><span id="_security_cryptology_gly"></span><span id="_SECURITY_CRYPTOLOGY_GLY"></span>**cryptology**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-307">Il ramo di matematica che comprende sia la crittografia che la crittanalisi.</span><span class="sxs-lookup"><span data-stu-id="1c15a-307">The branch of mathematics that encompasses both cryptography and cryptanalysis.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span><span class="sxs-lookup"><span data-stu-id="1c15a-308"><span id="_security_cryptospi_gly"></span><span id="_SECURITY_CRYPTOSPI_GLY"></span>**CryptoSPI**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-309">Interfaccia del programma di sistema utilizzata con un *provider del servizio di crittografia* (CSP).</span><span class="sxs-lookup"><span data-stu-id="1c15a-309">The system program interface used with a *cryptographic service provider* (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span><span class="sxs-lookup"><span data-stu-id="1c15a-310"><span id="_security_csp_gly"></span><span id="_SECURITY_CSP_GLY"></span>**CSP**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-311">Vedere *provider del servizio di crittografia*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-311">See *cryptographic service provider*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**Famiglia CSP**</span><span class="sxs-lookup"><span data-stu-id="1c15a-312"><span id="_security_csp_family_gly"></span><span id="_SECURITY_CSP_FAMILY_GLY"></span>**CSP family**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-313">Gruppo univoco di CSP che utilizzano lo stesso set di formati di dati ed eseguono la rispettiva funzione nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="1c15a-313">A unique group of CSPs that use the same set of data formats and perform their function in the same way.</span></span> <span data-ttu-id="1c15a-314">Anche quando due famiglie CSP utilizzano lo stesso algoritmo, ad esempio la crittografia a blocchi RC2, i diversi schemi di riempimento, lunghezze delle chiavi o modalità predefinite rendono ogni gruppo distinto.</span><span class="sxs-lookup"><span data-stu-id="1c15a-314">Even when two CSP families use the same algorithm (for example, the RC2 block cipher), their different padding schemes, keys lengths, or default modes make each group distinct.</span></span> <span data-ttu-id="1c15a-315">CryptoAPI è stato progettato in modo che ogni tipo di CSP rappresenti una famiglia particolare.</span><span class="sxs-lookup"><span data-stu-id="1c15a-315">CryptoAPI has been designed so that each CSP type represents a particular family.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**Nome CSP**</span><span class="sxs-lookup"><span data-stu-id="1c15a-316"><span id="_security_csp_name_gly"></span><span id="_SECURITY_CSP_NAME_GLY"></span>**CSP name**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-317">Nome testuale del CSP.</span><span class="sxs-lookup"><span data-stu-id="1c15a-317">The textual name of the CSP.</span></span> <span data-ttu-id="1c15a-318">Se il CSP è stato firmato da Microsoft, il nome deve corrispondere esattamente al nome del CSP specificato nel certificato di conformità dell'esportazione (ECC).</span><span class="sxs-lookup"><span data-stu-id="1c15a-318">If the CSP has been signed by Microsoft, this name must exactly match the CSP name that was specified in the Export Compliance Certificate (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**Tipo CSP**</span><span class="sxs-lookup"><span data-stu-id="1c15a-319"><span id="_security_csp_type_gly"></span><span id="_SECURITY_CSP_TYPE_GLY"></span>**CSP type**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-320">Indica la famiglia CSP associata a un provider.</span><span class="sxs-lookup"><span data-stu-id="1c15a-320">Indicates the CSP family associated with a provider.</span></span> <span data-ttu-id="1c15a-321">Quando un'applicazione si connette a un CSP di un determinato tipo, per impostazione predefinita ogni funzione CryptoAPI viene eseguita in base a quanto previsto dalla famiglia corrispondente a tale tipo di CSP.</span><span class="sxs-lookup"><span data-stu-id="1c15a-321">When an application connects to a CSP of a particular type, each of the CryptoAPI functions will, by default, operate in a way prescribed by the family that corresponds to that CSP type.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span><span class="sxs-lookup"><span data-stu-id="1c15a-322"><span id="_security_ctl_gly"></span><span id="_SECURITY_CTL_GLY"></span>**CTL**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-323">Vedere *elenco certificati attendibili*.</span><span class="sxs-lookup"><span data-stu-id="1c15a-323">See *certificate trust list*.</span></span>

</dd> <dt>

<span data-ttu-id="1c15a-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK ( \_ MEK)**</span><span class="sxs-lookup"><span data-stu-id="1c15a-324"><span id="_security_cylink_mek_gly"></span><span id="_SECURITY_CYLINK_MEK_GLY"></span>**CYLINK\_MEK**</span></span>
</dt> <dd>

<span data-ttu-id="1c15a-325">Algoritmo di crittografia che utilizza una variante a 40 bit di una chiave DES, dove 16 bit della chiave DES 56 bit sono impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="1c15a-325">An encryption algorithm that uses a 40-bit variant of a DES key where 16 bits of the 56-bit DES key are set to zero.</span></span> <span data-ttu-id="1c15a-326">Questo algoritmo viene implementato come specificato nella bozza IETF Specification for 40 bit DES.</span><span class="sxs-lookup"><span data-stu-id="1c15a-326">This algorithm is implemented as specified in the IETF Draft specification for 40-bit DES.</span></span> <span data-ttu-id="1c15a-327">La specifica bozza, al momento della stesura di questo documento, si trova in ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span><span class="sxs-lookup"><span data-stu-id="1c15a-327">The draft specification, at the time of this writing can be found at ftp://ftp.ietf.org/internet-drafts/draft-hoffman-des40-02.txt.</span></span> <span data-ttu-id="1c15a-328">Questo algoritmo viene usato con il valore di **\_ ID ALG** CALG \_ CYLINK \_ MEK.</span><span class="sxs-lookup"><span data-stu-id="1c15a-328">This algorithm is used with the **ALG\_ID** value CALG\_CYLINK\_MEK.</span></span>

</dd> </dl>

 

 
