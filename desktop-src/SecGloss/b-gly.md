---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316124"
---
# <a name="b-security-glossary"></a><span data-ttu-id="8bd9b-103">B (Glossario sulla sicurezza)</span><span class="sxs-lookup"><span data-stu-id="8bd9b-103">B (Security Glossary)</span></span>

<span data-ttu-id="8bd9b-104">[A](a-gly.md) B [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="8bd9b-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8bd9b-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**autorità di backup**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-106">Applicazione attendibile in esecuzione in un computer protetto che fornisce l'archiviazione secondaria per le chiavi di sessione dei client.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="8bd9b-107">L'autorità di backup archivia le chiavi della sessione come BLOB chiave crittografati con la chiave pubblica dell'autorità di backup.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**tipo di contenuto di base**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-109">Tipo di dati contenuti in un messaggio PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="8bd9b-110">I tipi di contenuto di base contengono solo dati, senza miglioramenti crittografici, ad esempio hash o firme.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="8bd9b-111">Attualmente, l'unico tipo di contenuto di base è il tipo di contenuto dei dati.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**funzioni di crittografia di base**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-113">Livello più basso di funzioni nell'architettura CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="8bd9b-114">Vengono usati dalle applicazioni e da altre funzioni CryptoAPI di alto livello per fornire l'accesso agli algoritmi di crittografia forniti da CSP, alla generazione di chiavi sicure e all'archiviazione sicura di segreti.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="8bd9b-115">Vedere anche [*provider del servizio di crittografia*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8bd9b-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Regole di codifica di base**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-117">BER Set di regole utilizzate per codificare i dati definiti ASN. 1 in un flusso di bit (zeri o uno) per l'archiviazione o la trasmissione esterna.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="8bd9b-118">Un singolo oggetto ASN. 1 può avere più codificazioni BER equivalenti.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="8bd9b-119">BER è definito nella raccomandazione CCITT X. 209.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="8bd9b-120">Si tratta di uno dei due metodi di codifica attualmente utilizzati da CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-122">Vedere *regole di codifica di base*.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big endian**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-124">Memoria o formato di dati in cui il byte più significativo viene archiviato nell'indirizzo inferiore o arriva per primo.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="8bd9b-125">Vedere anche [*Little-Endian*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8bd9b-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-127">Sequenza generica di bit che contengono una o più strutture di intestazione a lunghezza fissa più dati specifici del contesto.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="8bd9b-128">Vedere anche [*BLOB di chiavi*](k-gly.md), [*BLOB di certificati*](c-gly.md), BLOB del nome del [*certificato*](c-gly.md)e BLOB di [*attributi*](a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8bd9b-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**crittografia a blocchi**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-130">Algoritmo di crittografia che esegue la crittografia dei dati in unità discrete (denominate blocchi), anziché come un flusso continuo di bit.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="8bd9b-131">Le dimensioni del blocco più comuni sono di 64 bit.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="8bd9b-132">Ad esempio, DES è una crittografia a blocchi.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="8bd9b-133">Vedere anche [*crittografia del flusso*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8bd9b-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bd9b-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**chiave di crittografia bulk**</span><span class="sxs-lookup"><span data-stu-id="8bd9b-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="8bd9b-135">Chiave di sessione derivata da una chiave master.</span><span class="sxs-lookup"><span data-stu-id="8bd9b-135">A session key derived from a master key.</span></span> <span data-ttu-id="8bd9b-136">Le chiavi di crittografia bulk vengono usate nella crittografia [*Schannel*](s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8bd9b-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 



