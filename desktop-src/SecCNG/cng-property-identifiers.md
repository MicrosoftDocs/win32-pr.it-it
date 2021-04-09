---
description: Utilizzato con le funzioni BCryptGetProperty e BCryptSetProperty per identificare una proprietà.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificatori delle proprietà primitive di crittografia (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878614"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="6360b-103">Identificatori delle proprietà primitive di crittografia</span><span class="sxs-lookup"><span data-stu-id="6360b-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="6360b-104">Per identificare una proprietà vengono usati i valori seguenti con le funzioni [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) e [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .</span><span class="sxs-lookup"><span data-stu-id="6360b-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="6360b-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_nome dell'algoritmo BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-106">L "algorithmName"</span><span class="sxs-lookup"><span data-stu-id="6360b-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-107">Stringa Unicode con terminazione null che contiene il nome dell'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6360b-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_lunghezza del \_ tag di autenticazione BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-109">L "AuthTagLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-110">Lunghezze dei tag di autenticazione supportate dall'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6360b-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="6360b-111">Questa proprietà è una [**struttura \_ \_ \_ \_ struct di lunghezze di tag di autenticazione BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="6360b-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="6360b-112">Questa proprietà si applica solo agli algoritmi.</span><span class="sxs-lookup"><span data-stu-id="6360b-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_Lunghezza blocco \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-114">L "BlockLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-115">Dimensione, in byte, di un blocco di crittografia per l'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6360b-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="6360b-116">Questa proprietà si applica solo agli algoritmi di crittografia a blocchi.</span><span class="sxs-lookup"><span data-stu-id="6360b-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="6360b-117">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_ \_ elenco dimensioni blocco \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-119">L "BlockSizeList"</span><span class="sxs-lookup"><span data-stu-id="6360b-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-120">Elenco delle lunghezze dei blocchi supportate da un algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="6360b-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="6360b-121">Questo tipo di dati è una matrice di **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="6360b-122">Il numero di elementi nella matrice può essere determinato dividendo il numero di byte recuperati dalla dimensione di un singolo **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_modalità di concatenamento BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-124">L "ChainingMode"</span><span class="sxs-lookup"><span data-stu-id="6360b-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-125">Puntatore a una stringa Unicode con terminazione null che rappresenta la modalità di concatenamento dell'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="6360b-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="6360b-126">Questa proprietà può essere impostata su un handle di algoritmo o un handle di chiave per uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6360b-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="6360b-127">Identificatore</span><span class="sxs-lookup"><span data-stu-id="6360b-127">Identifier</span></span>                   | <span data-ttu-id="6360b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6360b-128">Value</span></span>                         | <span data-ttu-id="6360b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6360b-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6360b-130">**CBC (BCRYPT \_ Chain \_ mode) \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="6360b-131">L "ChainingModeCBC"</span><span class="sxs-lookup"><span data-stu-id="6360b-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="6360b-132">Imposta la modalità di concatenamento dell'algoritmo sul [*concatenamento dei blocchi crittografici*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="6360b-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="6360b-133">**\_ \_ CCM modalità a catena BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="6360b-134">L "ChainingModeCCM"</span><span class="sxs-lookup"><span data-stu-id="6360b-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="6360b-135">Imposta la modalità di concatenamento dell'algoritmo su Counter con la modalità CBC-MAC (CCM). **Windows Vista:** Questo valore è supportato a partire da Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="6360b-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="6360b-136">**\_modalità a catena BCRYPT \_ \_ CFB**</span><span class="sxs-lookup"><span data-stu-id="6360b-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="6360b-137">L "ChainingModeCFB"</span><span class="sxs-lookup"><span data-stu-id="6360b-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="6360b-138">Imposta la modalità di concatenamento dell'algoritmo su [*feedback crittografico*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="6360b-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="6360b-139">**BCRYPT \_ Chain \_ mode \_ BCE**</span><span class="sxs-lookup"><span data-stu-id="6360b-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="6360b-140">L "ChainingModeECB"</span><span class="sxs-lookup"><span data-stu-id="6360b-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="6360b-141">Imposta la modalità di concatenamento dell'algoritmo su [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).</span><span class="sxs-lookup"><span data-stu-id="6360b-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="6360b-142">**\_modalità a catena BCRYPT \_ \_ GCM**</span><span class="sxs-lookup"><span data-stu-id="6360b-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="6360b-143">L "ChainingModeGCM"</span><span class="sxs-lookup"><span data-stu-id="6360b-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="6360b-144">Imposta la modalità di concatenamento dell'algoritmo su Galois/Counter Mode (GCM). **Windows Vista:** Questo valore è supportato a partire da Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="6360b-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="6360b-145">**\_modalità a catena BCRYPT \_ \_ na**</span><span class="sxs-lookup"><span data-stu-id="6360b-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="6360b-146">L "ChainingModeN/A"</span><span class="sxs-lookup"><span data-stu-id="6360b-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="6360b-147">L'algoritmo non supporta il concatenamento.</span><span class="sxs-lookup"><span data-stu-id="6360b-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_parametri DH \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-149">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="6360b-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-150">Specifica i parametri da utilizzare con una chiave Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6360b-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="6360b-151">Questo tipo di dati è un puntatore a una struttura di [**\_ intestazione del \_ parametro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="6360b-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="6360b-152">Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.</span><span class="sxs-lookup"><span data-stu-id="6360b-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_parametri DSA \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-154">L "DSAParameters"</span><span class="sxs-lookup"><span data-stu-id="6360b-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-155">Specifica i parametri da usare con una chiave DSA.</span><span class="sxs-lookup"><span data-stu-id="6360b-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="6360b-156">Questa proprietà è un' [**\_ intestazione del \_ parametro \_ DSA BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) o una struttura dell' [**intestazione del \_ parametro DSA BCRYPT \_ \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="6360b-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="6360b-157">Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.</span><span class="sxs-lookup"><span data-stu-id="6360b-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="6360b-158">**Windows 8:** A partire da Windows 8, questa proprietà può essere una struttura [**BCRYPT \_ DSA \_ Parameter \_ header \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="6360b-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="6360b-159">Usare questa struttura se la dimensione della chiave supera 1024 bit ed è minore o uguale a 3072 bit.</span><span class="sxs-lookup"><span data-stu-id="6360b-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="6360b-160">Se la dimensione della chiave è maggiore o uguale a 512 ma minore o uguale a 1024 bit, usare la struttura [**dell' \_ \_ \_ intestazione del parametro BCRYPT DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="6360b-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_ \_ Lunghezza chiave effettiva \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-162">L "EffectiveKeyLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-163">Dimensione, in bit, della lunghezza effettiva di una chiave RC2.</span><span class="sxs-lookup"><span data-stu-id="6360b-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="6360b-164">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_ \_ Lunghezza blocco hash \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-166">L "HashBlockLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-167">Dimensione, in byte, del blocco per un hash.</span><span class="sxs-lookup"><span data-stu-id="6360b-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="6360b-168">Questa proprietà si applica solo agli algoritmi hash.</span><span class="sxs-lookup"><span data-stu-id="6360b-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="6360b-169">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_lunghezza hash \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-171">L "HashDigestLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-172">Dimensione, in byte, del valore hash di un provider hash.</span><span class="sxs-lookup"><span data-stu-id="6360b-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="6360b-173">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_elenco di \_ OID \_ hash BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-175">L "HashOIDList"</span><span class="sxs-lookup"><span data-stu-id="6360b-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-176">Elenco di [*identificatori di oggetti*](/windows/desktop/SecGloss/o-gly) hash codificati [*der*](/windows/desktop/SecGloss/d-gly)(OID).</span><span class="sxs-lookup"><span data-stu-id="6360b-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="6360b-177">Questa proprietà è una struttura dell' [**\_ \_ elenco di OID BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) .</span><span class="sxs-lookup"><span data-stu-id="6360b-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="6360b-178">Questa proprietà può essere letta solo.</span><span class="sxs-lookup"><span data-stu-id="6360b-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_vettore di inizializzazione BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="6360b-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-181">Contiene il [*vettore di inizializzazione*](/windows/desktop/SecGloss/i-gly) (IV) per una chiave.</span><span class="sxs-lookup"><span data-stu-id="6360b-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="6360b-182">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6360b-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_lunghezza della chiave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-184">L "lunghezza della lunghezza"</span><span class="sxs-lookup"><span data-stu-id="6360b-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-185">Dimensione, in bit, del valore della chiave di un provider di chiavi simmetriche.</span><span class="sxs-lookup"><span data-stu-id="6360b-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="6360b-186">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_lunghezze della chiave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-188">L "lunghezze della lunghezza"</span><span class="sxs-lookup"><span data-stu-id="6360b-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-189">Lunghezze delle chiavi supportate dall'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6360b-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="6360b-190">Questa proprietà è una [**struttura \_ \_ \_ struct della lunghezza della chiave BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="6360b-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="6360b-191">Questa proprietà si applica solo agli algoritmi.</span><span class="sxs-lookup"><span data-stu-id="6360b-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_lunghezza dell' \_ oggetto \_ chiave BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-193">L "KeyObjectLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-194">Questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6360b-194">This property is not used.</span></span> <span data-ttu-id="6360b-195">Per ottenere queste informazioni, viene usata la proprietà **BCRYPT \_ Object \_ length** .</span><span class="sxs-lookup"><span data-stu-id="6360b-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_complessità della chiave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-197">L "livello di attendibilità"</span><span class="sxs-lookup"><span data-stu-id="6360b-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-198">Numero di bit nella chiave.</span><span class="sxs-lookup"><span data-stu-id="6360b-198">The number of bits in the key.</span></span> <span data-ttu-id="6360b-199">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="6360b-200">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6360b-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_lunghezza del \_ blocco di messaggi BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-202">L "MessageBlockLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-203">Questo può essere impostato su qualsiasi handle di chiave con la modalità di concatenamento CFB impostata.</span><span class="sxs-lookup"><span data-stu-id="6360b-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="6360b-204">Per impostazione predefinita, questa proprietà è impostata su 1 per CFB a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="6360b-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="6360b-205">Se viene impostato sulla dimensione del blocco in byte, viene utilizzato il CFB di blocco completo.</span><span class="sxs-lookup"><span data-stu-id="6360b-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="6360b-206">Per le chiavi XTS, viene usato per impostare le dimensioni, in byte, dell'unità dati XTS (in genere 512 o 4096).</span><span class="sxs-lookup"><span data-stu-id="6360b-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_ \_ lunghezza MULTIoggetto \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-208">L "MultiObjectLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-209">Questa proprietà restituisce uno [**\_ struct di \_ \_ lunghezza BCRYPT \_ multioggetto**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)che contiene le informazioni necessarie per calcolare le dimensioni di un buffer di oggetti.</span><span class="sxs-lookup"><span data-stu-id="6360b-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="6360b-210">Questa proprietà è supportata solo nelle versioni del sistema operativo che supportano la funzione [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .</span><span class="sxs-lookup"><span data-stu-id="6360b-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_lunghezza dell'oggetto BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-212">L "ObjectLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-213">Dimensione, in byte, del sottooggetto di un provider.</span><span class="sxs-lookup"><span data-stu-id="6360b-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="6360b-214">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="6360b-215">Attualmente, i provider di algoritmi di crittografia hash e simmetrico utilizzano buffer allocati dal chiamante per archiviare i relativi oggetti sottooggetti.</span><span class="sxs-lookup"><span data-stu-id="6360b-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="6360b-216">Per il provider hash, ad esempio, è necessario allocare memoria per l'oggetto hash ottenuto con la funzione [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="6360b-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="6360b-217">Questa proprietà fornisce le dimensioni del buffer per l'oggetto di un provider, in modo da poter allocare memoria per l'oggetto creato dal provider.</span><span class="sxs-lookup"><span data-stu-id="6360b-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_schemi di riempimento BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-219">L "PaddingSchemes"</span><span class="sxs-lookup"><span data-stu-id="6360b-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-220">Rappresenta lo schema di riempimento del provider di algoritmi RSA.</span><span class="sxs-lookup"><span data-stu-id="6360b-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="6360b-221">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="6360b-222">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6360b-222">This can be one of the following values.</span></span>



| <span data-ttu-id="6360b-223">Identificatore</span><span class="sxs-lookup"><span data-stu-id="6360b-223">Identifier</span></span>                             | <span data-ttu-id="6360b-224">Valore</span><span class="sxs-lookup"><span data-stu-id="6360b-224">Value</span></span>      | <span data-ttu-id="6360b-225">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6360b-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="6360b-226">**\_router di \_ riempimento \_ supportato da BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="6360b-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6360b-227">0x00000001</span></span> | <span data-ttu-id="6360b-228">Il provider supporta la spaziatura interna aggiunta dal router.</span><span class="sxs-lookup"><span data-stu-id="6360b-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="6360b-229">**BCRYPT \_ \_ Pad supportato \_ PKCS1 \_ enc**</span><span class="sxs-lookup"><span data-stu-id="6360b-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="6360b-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6360b-230">0x00000002</span></span> | <span data-ttu-id="6360b-231">Il provider supporta lo schema di riempimento della crittografia PKCS1.</span><span class="sxs-lookup"><span data-stu-id="6360b-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="6360b-232">**BCRYPT \_ \_ Pad supportato \_ PKCS1 \_ sig**</span><span class="sxs-lookup"><span data-stu-id="6360b-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="6360b-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6360b-233">0x00000004</span></span> | <span data-ttu-id="6360b-234">Il provider supporta lo schema di riempimento della firma PKCS1.</span><span class="sxs-lookup"><span data-stu-id="6360b-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="6360b-235">**\_ \_ OAEP Pad supportato da BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="6360b-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6360b-236">0x00000008</span></span> | <span data-ttu-id="6360b-237">Il provider supporta lo schema di riempimento OAEP.</span><span class="sxs-lookup"><span data-stu-id="6360b-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="6360b-238">**BCRYPT \_ Pad supportato da \_ \_ PSS**</span><span class="sxs-lookup"><span data-stu-id="6360b-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="6360b-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6360b-239">0x00000010</span></span> | <span data-ttu-id="6360b-240">Il provider supporta lo schema di riempimento PSS.</span><span class="sxs-lookup"><span data-stu-id="6360b-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_handle del provider BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="6360b-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-242">L "ProviderHandle"</span><span class="sxs-lookup"><span data-stu-id="6360b-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-243">Handle del provider CNG che ha creato l'oggetto passato nel parametro *hObject* .</span><span class="sxs-lookup"><span data-stu-id="6360b-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="6360b-244">Questo tipo di dati è **un \_ \_ handle BCRYPT ALG**.</span><span class="sxs-lookup"><span data-stu-id="6360b-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="6360b-245">Questa proprietà può essere recuperata solo. non può essere impostata.</span><span class="sxs-lookup"><span data-stu-id="6360b-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6360b-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**\_lunghezza firma \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="6360b-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6360b-247">L "SignatureLength"</span><span class="sxs-lookup"><span data-stu-id="6360b-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="6360b-248">Dimensione, in byte, della lunghezza di una firma per una chiave.</span><span class="sxs-lookup"><span data-stu-id="6360b-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="6360b-249">Questo tipo di dati è un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6360b-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="6360b-250">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6360b-250">This property only applies to keys.</span></span> <span data-ttu-id="6360b-251">Questa proprietà può essere recuperata solo. non può essere impostata.</span><span class="sxs-lookup"><span data-stu-id="6360b-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6360b-252">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6360b-252">Requirements</span></span>



| <span data-ttu-id="6360b-253">Requisito</span><span class="sxs-lookup"><span data-stu-id="6360b-253">Requirement</span></span> | <span data-ttu-id="6360b-254">Valore</span><span class="sxs-lookup"><span data-stu-id="6360b-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6360b-255">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6360b-255">Minimum supported client</span></span><br/> | <span data-ttu-id="6360b-256">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6360b-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6360b-257">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6360b-257">Minimum supported server</span></span><br/> | <span data-ttu-id="6360b-258">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6360b-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6360b-259">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6360b-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="6360b-260"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="6360b-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 

