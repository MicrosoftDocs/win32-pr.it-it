---
description: Utilizzato per identificare una proprietà di archiviazione delle chiavi.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificatori di proprietà di archiviazione chiavi (ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319389"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="69b3f-103">Identificatori delle proprietà di archiviazione chiavi</span><span class="sxs-lookup"><span data-stu-id="69b3f-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="69b3f-104">Per identificare una proprietà di archiviazione delle chiavi vengono usati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="69b3f-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_proprietà del \_ gruppo di algoritmi NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-106">L "gruppo di algoritmi"</span><span class="sxs-lookup"><span data-stu-id="69b3f-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-107">Stringa Unicode con terminazione null che contiene il nome del gruppo di algoritmi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="69b3f-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="69b3f-108">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-108">This property only applies to keys.</span></span> <span data-ttu-id="69b3f-109">Il provider di archiviazione chiavi Microsoft restituisce gli identificatori seguenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="69b3f-110">Identificatore</span><span class="sxs-lookup"><span data-stu-id="69b3f-110">Identifier</span></span>                                     | <span data-ttu-id="69b3f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-111">Value</span></span>              | <span data-ttu-id="69b3f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b3f-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="69b3f-113">**\_gruppo di \_ algoritmi \_ RSA NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="69b3f-114">RSA</span><span class="sxs-lookup"><span data-stu-id="69b3f-114">"RSA"</span></span><br/>   | <span data-ttu-id="69b3f-115">Gruppo di algoritmi RSA.</span><span class="sxs-lookup"><span data-stu-id="69b3f-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="69b3f-116">**\_gruppo di \_ algoritmi NCRYPT DH \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="69b3f-117">DH</span><span class="sxs-lookup"><span data-stu-id="69b3f-117">"DH"</span></span><br/>    | <span data-ttu-id="69b3f-118">Gruppo di algoritmi di Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="69b3f-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="69b3f-119">**\_gruppo di \_ algoritmi NCRYPT DSA \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="69b3f-120">DSA</span><span class="sxs-lookup"><span data-stu-id="69b3f-120">"DSA"</span></span><br/>   | <span data-ttu-id="69b3f-121">Gruppo di algoritmi DSA.</span><span class="sxs-lookup"><span data-stu-id="69b3f-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="69b3f-122">**\_gruppo di \_ algoritmi NCRYPT ECDSA \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="69b3f-123">ECDSA</span><span class="sxs-lookup"><span data-stu-id="69b3f-123">"ECDSA"</span></span><br/> | <span data-ttu-id="69b3f-124">Gruppo di algoritmi DSA a curva ellittica.</span><span class="sxs-lookup"><span data-stu-id="69b3f-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="69b3f-125">**\_gruppo di \_ algoritmi NCRYPT ECDH \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="69b3f-126">ECDH</span><span class="sxs-lookup"><span data-stu-id="69b3f-126">"ECDH"</span></span><br/>  | <span data-ttu-id="69b3f-127">La curva ellittica Diffie-Hellman gruppo di algoritmi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_proprietà dell'algoritmo NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-129">L "Nome algoritmo"</span><span class="sxs-lookup"><span data-stu-id="69b3f-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-130">Stringa Unicode con terminazione null che contiene il nome dell'algoritmo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="69b3f-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="69b3f-131">Può trattarsi di uno degli [**identificatori di algoritmo CNG**](cng-algorithm-identifiers.md) predefiniti o di un altro identificatore dell'algoritmo registrato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="69b3f-132">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_ \_ chiave ECDH associata \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-134">L "SmartCardAssociatedECDHKey"</span><span class="sxs-lookup"><span data-stu-id="69b3f-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-135">Valore **LPWSTR** che indica il nome del contenitore della chiave ellittica Diffie-Hellman (ECDH) da utilizzare durante l'accesso per un handle specificato a una chiave ECDSA (Digital Signature Algorithm) a curva ellittica.</span><span class="sxs-lookup"><span data-stu-id="69b3f-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="69b3f-136">Se non sono presenti chiavi di ECDH sulla scheda, il [*provider di archiviazione chiavi*](/windows/desktop/SecGloss/k-gly) (KSP) restituisce **nte \_ non \_ trovato**.</span><span class="sxs-lookup"><span data-stu-id="69b3f-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="69b3f-137">Questa proprietà si applica alle chiavi di ECDSA per l'accesso con smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="69b3f-138">La proprietà è supportata dal provider di archiviazione chiavi per Smart Card Microsoft e non dal provider di archiviazione chiavi software Microsoft.</span><span class="sxs-lookup"><span data-stu-id="69b3f-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="69b3f-139">**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_ \_ proprietà Lunghezza blocco \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-141">L "lunghezza del blocco"</span><span class="sxs-lookup"><span data-stu-id="69b3f-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-142">**Valore DWORD** che contiene la lunghezza, in byte, del blocco di crittografia.</span><span class="sxs-lookup"><span data-stu-id="69b3f-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="69b3f-143">Questa proprietà si applica solo alle chiavi che supportano la crittografia.</span><span class="sxs-lookup"><span data-stu-id="69b3f-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_proprietà del certificato NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-145">L "SmartCardKeyCertificate"</span><span class="sxs-lookup"><span data-stu-id="69b3f-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-146">Un [*BLOB*](/windows/desktop/SecGloss/b-gly) che contiene un certificato X. 509 associato alla chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="69b3f-147">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** [*BLOB*](/windows/desktop/SecGloss/b-gly) contenente il [*certificato*](/windows/desktop/SecGloss/c-gly)della chiave della [*Smart Card*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="69b3f-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="69b3f-148">Questa proprietà non è supportata dal provider di archiviazione chiavi del software Microsoft.</span><span class="sxs-lookup"><span data-stu-id="69b3f-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**\_ \_ Proprietà parametri DH \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-150">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="69b3f-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-151">Specifica i parametri da utilizzare con una chiave Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="69b3f-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="69b3f-152">Questo tipo di dati è un puntatore a una struttura di [**\_ intestazione del \_ parametro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="69b3f-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="69b3f-153">Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**\_proprietà dei \_ criteri di esportazione NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-155">L "Esporta criteri"</span><span class="sxs-lookup"><span data-stu-id="69b3f-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-156">**Valore DWORD** che contiene un set di flag che specificano i criteri di esportazione per una chiave permanente.</span><span class="sxs-lookup"><span data-stu-id="69b3f-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="69b3f-157">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-157">This property only applies to keys.</span></span> <span data-ttu-id="69b3f-158">Può contenere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="69b3f-159">Identificatore</span><span class="sxs-lookup"><span data-stu-id="69b3f-159">Identifier</span></span>                                    | <span data-ttu-id="69b3f-160">Valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-160">Value</span></span>      | <span data-ttu-id="69b3f-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b3f-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b3f-162">**\_flag NCRYPT Consenti \_ esportazione \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="69b3f-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="69b3f-163">0x00000001</span></span> | <span data-ttu-id="69b3f-164">La chiave privata può essere esportata.</span><span class="sxs-lookup"><span data-stu-id="69b3f-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="69b3f-165">**NCRYPT \_ Consenti \_ \_ flag di esportazione testo non crittografato \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="69b3f-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="69b3f-166">0x00000002</span></span> | <span data-ttu-id="69b3f-167">La chiave privata può essere esportata in formato testo normale.</span><span class="sxs-lookup"><span data-stu-id="69b3f-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="69b3f-168">**NCRYPT \_ consente il \_ flag di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="69b3f-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="69b3f-169">0x00000004</span></span> | <span data-ttu-id="69b3f-170">La chiave privata può essere esportata una sola volta a scopo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69b3f-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="69b3f-171">Questo flag si applica solo all'handle di chiave originale su cui è impostato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="69b3f-172">Questo criterio può essere applicato solo all'handle di chiave originale.</span><span class="sxs-lookup"><span data-stu-id="69b3f-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="69b3f-173">Dopo la chiusura dell'handle di chiave, la chiave non può più essere esportata a scopo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69b3f-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="69b3f-174">**NCRYPT \_ consente \_ un \_ flag di archiviazione in testo non crittografato \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="69b3f-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="69b3f-175">0x00000008</span></span> | <span data-ttu-id="69b3f-176">La chiave privata può essere esportata una sola volta in formato testo non crittografato a scopo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69b3f-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="69b3f-177">Questo flag si applica solo all'handle di chiave originale su cui è impostato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="69b3f-178">Questo criterio può essere applicato solo all'handle di chiave originale.</span><span class="sxs-lookup"><span data-stu-id="69b3f-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="69b3f-179">Dopo la chiusura dell'handle di chiave, la chiave non può più essere esportata a scopo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69b3f-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_proprietà di \_ tipo \_ impl di NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-181">L "tipo di impl"</span><span class="sxs-lookup"><span data-stu-id="69b3f-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-182">**Valore DWORD** che contiene un set di flag che definiscono i dettagli di implementazione del provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="69b3f-183">Questa proprietà si applica solo ai provider di archiviazione chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="69b3f-184">Può contenere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="69b3f-185">Identificatore</span><span class="sxs-lookup"><span data-stu-id="69b3f-185">Identifier</span></span>                            | <span data-ttu-id="69b3f-186">Valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-186">Value</span></span>      | <span data-ttu-id="69b3f-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b3f-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="69b3f-188">**\_ \_ flag hardware NCRYPT \_ impl**</span><span class="sxs-lookup"><span data-stu-id="69b3f-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="69b3f-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="69b3f-189">0x00000001</span></span> | <span data-ttu-id="69b3f-190">Il provider è basato su hardware.</span><span class="sxs-lookup"><span data-stu-id="69b3f-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="69b3f-191">**\_ \_ flag software NCRYPT \_ impl**</span><span class="sxs-lookup"><span data-stu-id="69b3f-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="69b3f-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="69b3f-192">0x00000002</span></span> | <span data-ttu-id="69b3f-193">Il provider è basato su software.</span><span class="sxs-lookup"><span data-stu-id="69b3f-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="69b3f-194">**\_ \_ flag rimovibile impl NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="69b3f-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="69b3f-195">0x00000008</span></span> | <span data-ttu-id="69b3f-196">Il provider è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="69b3f-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="69b3f-197">**\_ \_ \_ flag RNG hardware NCRYPT \_ impl**</span><span class="sxs-lookup"><span data-stu-id="69b3f-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="69b3f-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="69b3f-198">0x00000010</span></span> | <span data-ttu-id="69b3f-199">Il provider è un generatore di numeri casuali basato su hardware.</span><span class="sxs-lookup"><span data-stu-id="69b3f-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_proprietà del \_ tipo di chiave NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-201">L "tipo di chiave"</span><span class="sxs-lookup"><span data-stu-id="69b3f-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-202">**Valore DWORD** che contiene un set di flag che definiscono il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="69b3f-203">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-203">This property only applies to keys.</span></span> <span data-ttu-id="69b3f-204">Può contenere zero o il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="69b3f-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="69b3f-205">Identificatore</span><span class="sxs-lookup"><span data-stu-id="69b3f-205">Identifier</span></span>                     | <span data-ttu-id="69b3f-206">Valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-206">Value</span></span>      | <span data-ttu-id="69b3f-207">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b3f-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b3f-208">**\_ \_ flag chiave del computer NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="69b3f-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="69b3f-209">0x00000001</span></span> | <span data-ttu-id="69b3f-210">La chiave si applica al computer locale.</span><span class="sxs-lookup"><span data-stu-id="69b3f-210">The key applies to the local computer.</span></span> <span data-ttu-id="69b3f-211">Se questo flag non è presente, la chiave si applica all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="69b3f-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_ \_ Proprietà utilizzo chiavi \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-213">L "utilizzo chiave"</span><span class="sxs-lookup"><span data-stu-id="69b3f-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-214">**DWORD** che contiene un set di flag che definiscono i dettagli di utilizzo per una chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="69b3f-215">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-215">This property only applies to keys.</span></span> <span data-ttu-id="69b3f-216">Può contenere zero o una combinazione di uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="69b3f-217">Identificatore</span><span class="sxs-lookup"><span data-stu-id="69b3f-217">Identifier</span></span>                              | <span data-ttu-id="69b3f-218">Valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-218">Value</span></span>      | <span data-ttu-id="69b3f-219">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b3f-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="69b3f-220">**NCRYPT \_ Consenti \_ flag di decrittografia \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="69b3f-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="69b3f-221">0x00000001</span></span> | <span data-ttu-id="69b3f-222">La chiave può essere usata per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="69b3f-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="69b3f-223">**NCRYPT \_ Consenti \_ flag di firma \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="69b3f-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="69b3f-224">0x00000002</span></span> | <span data-ttu-id="69b3f-225">La chiave può essere usata per la firma.</span><span class="sxs-lookup"><span data-stu-id="69b3f-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="69b3f-226">**NCRYPT \_ il \_ \_ flag di accettazione del tasto \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="69b3f-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="69b3f-227">0x00000004</span></span> | <span data-ttu-id="69b3f-228">La chiave può essere utilizzata per la crittografia dei contratti di segreto.</span><span class="sxs-lookup"><span data-stu-id="69b3f-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="69b3f-229">**NCRYPT \_ consente \_ tutti gli \_ utilizzi**</span><span class="sxs-lookup"><span data-stu-id="69b3f-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="69b3f-230">0x00FFFFFF</span><span class="sxs-lookup"><span data-stu-id="69b3f-230">0x00ffffff</span></span> | <span data-ttu-id="69b3f-231">La chiave può essere usata per qualsiasi scopo.</span><span class="sxs-lookup"><span data-stu-id="69b3f-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT \_ Ultima \_ \_ proprietà modificata**</span><span class="sxs-lookup"><span data-stu-id="69b3f-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-233">L "modificato"</span><span class="sxs-lookup"><span data-stu-id="69b3f-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-234">Indica la data dell'Ultima modifica apportata alla chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="69b3f-235">Questo tipo di dati è un puntatore a una struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="69b3f-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="69b3f-236">Questa proprietà si applica solo alle chiavi salvate in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="69b3f-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_proprietà Length di NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-238">L "lunghezza"</span><span class="sxs-lookup"><span data-stu-id="69b3f-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-239">**Valore DWORD** che contiene la lunghezza, in bit, della chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="69b3f-240">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_Proprietà lunghezze NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-242">L "lunghezze"</span><span class="sxs-lookup"><span data-stu-id="69b3f-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-243">Indica le dimensioni delle chiavi supportate dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="69b3f-244">Questo tipo di dati è un puntatore a una struttura di [**\_ \_ lunghezza supportata da NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) che contiene queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="69b3f-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="69b3f-245">Questa proprietà si applica solo alle chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_ \_ \_ proprietà lunghezza max nome \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-247">L "lunghezza massima del nome"</span><span class="sxs-lookup"><span data-stu-id="69b3f-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-248">**Valore DWORD** che contiene la lunghezza massima, in caratteri, del nome di una chiave persistente.</span><span class="sxs-lookup"><span data-stu-id="69b3f-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="69b3f-249">Questa proprietà si applica solo a un provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-249">This property only applies to a provider.</span></span>

<span data-ttu-id="69b3f-250">Questa proprietà è destinata principalmente a essere usata dai provider di archiviazione chiavi che archiviano le chiavi in un dispositivo con una quantità limitata di memoria disponibile, ad esempio una smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_proprietà Name di NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-252">L "nome"</span><span class="sxs-lookup"><span data-stu-id="69b3f-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-253">Puntatore a una stringa Unicode con terminazione null che contiene il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="69b3f-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**\_ \_ proprietà richiesta PIN \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-255">L "SmartCardPinPrompt"</span><span class="sxs-lookup"><span data-stu-id="69b3f-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-256">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_Proprietà pin \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-258">L "SmartCardPin"</span><span class="sxs-lookup"><span data-stu-id="69b3f-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-259">Puntatore a una stringa Unicode con terminazione null che contiene il PIN.</span><span class="sxs-lookup"><span data-stu-id="69b3f-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="69b3f-260">Il PIN viene usato per una chiave della smart card o la password per una chiave protetta da password archiviata in un provider di archiviazione chiavi basato su software.</span><span class="sxs-lookup"><span data-stu-id="69b3f-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="69b3f-261">Questa proprietà può essere impostata solo.</span><span class="sxs-lookup"><span data-stu-id="69b3f-261">This property can only be set.</span></span> <span data-ttu-id="69b3f-262">Microsoft KSP memorizza nella cache questo valore in modo che l'utente venga richiesto una sola volta per processo.</span><span class="sxs-lookup"><span data-stu-id="69b3f-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_ \_ proprietà Handle provider \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-264">L "handle del provider"</span><span class="sxs-lookup"><span data-stu-id="69b3f-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-265">**Handle NCRYPT \_ prova \_** contenente l'handle del provider di archiviazione chiavi CNG.</span><span class="sxs-lookup"><span data-stu-id="69b3f-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="69b3f-266">Al termine dell'utilizzo dell'handle, è necessario chiamare [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) per rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="69b3f-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_Proprietà Reader \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-268">L "SmartCardReader"</span><span class="sxs-lookup"><span data-stu-id="69b3f-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-269">Puntatore a una stringa Unicode con terminazione null che contiene il nome del lettore di smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="69b3f-270">Questa proprietà può essere impostata solo.</span><span class="sxs-lookup"><span data-stu-id="69b3f-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ Proprietà CERTSTORE radice \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-272">L "SmartcardRootCertStore"</span><span class="sxs-lookup"><span data-stu-id="69b3f-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-273">Oggetto **HCERTSTORE** che rappresenta l'archivio certificati radice della smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ ID pin spaventato**</span><span class="sxs-lookup"><span data-stu-id="69b3f-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-275">L "SmartCardPinId"</span><span class="sxs-lookup"><span data-stu-id="69b3f-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-276">Puntatore al valore dell' **\_ ID pin** associato a una [*chiave crittografica*](/windows/desktop/SecGloss/c-gly) specificata in una [*Smart Card*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="69b3f-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="69b3f-277">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="69b3f-277">This is a read-only property.</span></span> <span data-ttu-id="69b3f-278">Il tipo di dati **pin \_ ID** è definito in cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="69b3f-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="69b3f-279">**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_ \_ informazioni sul pin spaventato \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-281">L "SmartCardPinInfo"</span><span class="sxs-lookup"><span data-stu-id="69b3f-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-282">Puntatore per aggiungere la struttura di [**\_ informazioni**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) del PIN associato a una chiave crittografica specificata nella smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="69b3f-283">Il chiamante fornisce l'handle di chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-283">The caller provides the key handle.</span></span> <span data-ttu-id="69b3f-284">Questa proprietà è una proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="69b3f-284">This property is a read-only property.</span></span> <span data-ttu-id="69b3f-285">La struttura delle **\_ informazioni sul pin** è definita in cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="69b3f-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="69b3f-286">**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="69b3f-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_Proprietà NCRYPT Secure \_ pin \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-288">L "SmartCardSecurePin"</span><span class="sxs-lookup"><span data-stu-id="69b3f-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-289">Puntatore a una stringa Unicode con terminazione null che contiene il PIN della sessione della smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="69b3f-290">Questa proprietà può essere impostata solo.</span><span class="sxs-lookup"><span data-stu-id="69b3f-290">This property can only be set.</span></span>

<span data-ttu-id="69b3f-291">**Windows Vista:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="69b3f-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**\_ \_ Proprietà descr NCRYPT \_ Security**</span><span class="sxs-lookup"><span data-stu-id="69b3f-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-293">L "descr di sicurezza"</span><span class="sxs-lookup"><span data-stu-id="69b3f-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-294">Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene informazioni sul controllo di accesso per la chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="69b3f-295">Questa proprietà si applica solo alle chiavi permanenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="69b3f-296">Il parametro *dwFlags* della funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) o [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica la parte del descrittore di sicurezza da ottenere o impostare.</span><span class="sxs-lookup"><span data-stu-id="69b3f-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**Proprietà di supporto di NCRYPT \_ Security \_ Descr \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-298">L "supporto del descr di sicurezza"</span><span class="sxs-lookup"><span data-stu-id="69b3f-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-299">Indica se il provider supporta i descrittori di sicurezza per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="69b3f-300">Questa proprietà è un **valore DWORD** che contiene 1 se il provider supporta descrittori di sicurezza per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="69b3f-301">Se questa proprietà contiene qualsiasi altro valore o se la funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) restituisce **nte \_ non \_ supportata**, il provider non supporta i descrittori di sicurezza per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="69b3f-302">Questa proprietà si applica solo ai provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_proprietà GUID Smart Card NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-304">L "SmartCardGuid"</span><span class="sxs-lookup"><span data-stu-id="69b3f-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-305">BLOB contenente l'identificatore della smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_proprietà dei \_ criteri dell'interfaccia utente di NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-307">L "criteri dell'interfaccia utente"</span><span class="sxs-lookup"><span data-stu-id="69b3f-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-308">Se usato con la funzione [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) o [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , si tratta di un puntatore a una struttura di [**\_ \_ criteri dell'**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) interfaccia utente NCRYPT che contiene i criteri di interfaccia utente chiave avanzata per la chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="69b3f-309">Questa proprietà si applica solo alle chiavi permanenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="69b3f-310">Questa proprietà può essere impostata solo al momento della generazione della chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="69b3f-311">Una volta chiamata la funzione [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) per questa chiave, questa proprietà diventa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="69b3f-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="69b3f-312">Un provider di archiviazione chiavi può ricevere questo parametro tramite una funzione di callback [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) .</span><span class="sxs-lookup"><span data-stu-id="69b3f-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="69b3f-313">Il valore del parametro è una \_ \_ struttura BLOB di criteri dell'interfaccia utente NCRYPT \_ che contiene le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="69b3f-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="69b3f-314">Analogamente, quando un'applicazione effettua una richiesta tramite NCryptSetPropertyFn al provider per restituire questa proprietà, è previsto che il provider restituisca una \_ struttura del BLOB dei criteri dell'interfaccia utente di NCRYPT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="69b3f-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_ \_ proprietà nome univoco \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-316">L "nome univoco"</span><span class="sxs-lookup"><span data-stu-id="69b3f-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-317">Puntatore a una stringa Unicode con terminazione null che contiene il nome univoco dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="69b3f-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="69b3f-318">Si tratta di un nome alternativo che può essere usato per accedere alla chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="69b3f-319">Questa proprietà viene usata quando si pensa che il nome della chiave passato in origine a [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) non sia sufficiente per identificare in modo affidabile la chiave salvata in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="69b3f-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="69b3f-320">Il provider di archiviazione chiavi Microsoft restituirà il nome del file della chiave come questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="69b3f-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ utilizzare \_ la \_ proprietà di contesto**</span><span class="sxs-lookup"><span data-stu-id="69b3f-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-322">L "USA contesto"</span><span class="sxs-lookup"><span data-stu-id="69b3f-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-323">Puntatore a una stringa Unicode con terminazione null che descrive il contesto dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="69b3f-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="69b3f-324">Questa proprietà non è persistente e può essere impostata su un provider o una chiave.</span><span class="sxs-lookup"><span data-stu-id="69b3f-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="69b3f-325">Una chiave non ha accesso alla proprietà della **\_ proprietà di \_ contesto \_ use NCRYPT** del provider perché la proprietà è specifica solo per l'handle per cui è impostata.</span><span class="sxs-lookup"><span data-stu-id="69b3f-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="69b3f-326">Un esempio in cui questa proprietà verrebbe usata nel contesto di un provider è un provider di archiviazione chiavi che deve richiedere all'utente durante una chiamata a [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (ad esempio, "inserire la smart card nel lettore").</span><span class="sxs-lookup"><span data-stu-id="69b3f-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="69b3f-327">Poiché l'handle di chiave non è disponibile fino a quando **NCryptOpenKey** non restituisce, l'applicazione deve impostare questa proprietà sull'handle del provider prima di chiamare **NCryptOpenKey**.</span><span class="sxs-lookup"><span data-stu-id="69b3f-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="69b3f-328">Un esempio in cui questa proprietà verrebbe usata nel contesto di un handle di chiave è un provider di archiviazione chiavi che deve richiedere all'utente durante un'operazione usando la chiave (ad esempio, "questa applicazione deve usare questa chiave per firmare un documento").</span><span class="sxs-lookup"><span data-stu-id="69b3f-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="69b3f-329">Il provider potrebbe quindi inoltrare queste informazioni di contesto all'utente in qualsiasi interfaccia utente visualizzata durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="69b3f-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_Proprietà NCRYPT use \_ Count \_ Enabled \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-331">L "numero di utilizzi abilitati"</span><span class="sxs-lookup"><span data-stu-id="69b3f-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-332">Indica se il provider supporta il conteggio dell'utilizzo per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="69b3f-333">Questa proprietà è un **valore DWORD** che contiene 1 se il provider supporta il conteggio dell'utilizzo per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="69b3f-334">Se questa proprietà contiene qualsiasi altro valore o se la funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) restituisce **nte \_ non \_ supportata**, il provider non supporta il conteggio dell'utilizzo per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="69b3f-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="69b3f-335">Questa proprietà si applica solo ai provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_ \_ Proprietà conteggio utilizzo \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-337">L "conteggio utilizzo"</span><span class="sxs-lookup"><span data-stu-id="69b3f-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-338">Variabile [**di \_ tipo Integer ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) che contiene il numero di operazioni eseguite dalla [*chiave privata*](/windows/desktop/SecGloss/p-gly) specificata.</span><span class="sxs-lookup"><span data-stu-id="69b3f-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="69b3f-339">Questa proprietà è facoltativa e potrebbe non essere supportata da tutti i provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="69b3f-340">I provider che supportano questa proprietà nelle chiavi devono supportare anche la proprietà della **\_ Proprietà NCRYPT use \_ Count \_ Enabled \_** nell'handle del provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="69b3f-341">Il provider di archiviazione chiavi Microsoft non supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="69b3f-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="69b3f-342">Questa proprietà si applica solo alle chiavi permanenti.</span><span class="sxs-lookup"><span data-stu-id="69b3f-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_Proprietà CERTSTORE dell'utente NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-344">L "SmartCardUserCertStore"</span><span class="sxs-lookup"><span data-stu-id="69b3f-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-345">Oggetto **HCERTSTORE** che rappresenta l'archivio certificati utente della smart card.</span><span class="sxs-lookup"><span data-stu-id="69b3f-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_proprietà della versione NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="69b3f-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-347">L "versione"</span><span class="sxs-lookup"><span data-stu-id="69b3f-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-348">**Valore DWORD** che contiene la versione software del provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="69b3f-349">La parola alta contiene la versione principale e la parola bassa contiene la versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="69b3f-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="69b3f-350">Ad esempio, 0x00030033 = 3,51.</span><span class="sxs-lookup"><span data-stu-id="69b3f-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="69b3f-351">Questa proprietà si applica solo ai provider.</span><span class="sxs-lookup"><span data-stu-id="69b3f-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="69b3f-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_ \_ Proprietà handle finestra \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="69b3f-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69b3f-353">L "handle HWND"</span><span class="sxs-lookup"><span data-stu-id="69b3f-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="69b3f-354">Puntatore all'handle della finestra (**HWND**) da utilizzare come elemento padre di qualsiasi interfaccia utente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="69b3f-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="69b3f-355">Poiché è possibile che si verifichi un comportamento indesiderato quando un'interfaccia utente viene visualizzata utilizzando un handle di finestra **null** per l'elemento padre, è consigliabile che un provider di archiviazione chiavi non visualizzi un'interfaccia utente a meno che questa proprietà non sia impostata.</span><span class="sxs-lookup"><span data-stu-id="69b3f-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="69b3f-356">I valori seguenti vengono utilizzati per definire i limiti dei dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="69b3f-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="69b3f-357">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="69b3f-358">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b3f-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="69b3f-359"><dt>**NCRYPT \_ Numero \_ massimo \_**</dt> di <dt>0x100000</dt> dati della proprietà</span><span class="sxs-lookup"><span data-stu-id="69b3f-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="69b3f-360">Specifica la dimensione massima in byte del valore di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="69b3f-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="69b3f-361"><dt>**NCRYPT \_ \_ \_ Nome di proprietà Max**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="69b3f-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="69b3f-362">Specifica la dimensione massima del nome di una proprietà, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="69b3f-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="69b3f-363">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69b3f-363">Requirements</span></span>



| <span data-ttu-id="69b3f-364">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b3f-364">Requirement</span></span> | <span data-ttu-id="69b3f-365">Valore</span><span class="sxs-lookup"><span data-stu-id="69b3f-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="69b3f-366">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69b3f-366">Minimum supported client</span></span><br/> | <span data-ttu-id="69b3f-367">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69b3f-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="69b3f-368">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69b3f-368">Minimum supported server</span></span><br/> | <span data-ttu-id="69b3f-369">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69b3f-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="69b3f-370">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69b3f-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b3f-371"><dt>Ncrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b3f-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b3f-372">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69b3f-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b3f-373">**NCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="69b3f-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="69b3f-374">**NCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="69b3f-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

