---
description: "A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia dai provider di archiviazione chiavi."
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Provider di algoritmi di crittografia CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315410"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="973ff-103">Provider di algoritmi di crittografia CNG</span><span class="sxs-lookup"><span data-stu-id="973ff-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="973ff-104">A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia dai provider di archiviazione chiavi.</span><span class="sxs-lookup"><span data-stu-id="973ff-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="973ff-105">Le operazioni di base sugli algoritmi di crittografia, ad esempio l'hashing e la firma, sono denominate operazioni primitive o semplici primitive.</span><span class="sxs-lookup"><span data-stu-id="973ff-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="973ff-106">CNG include un provider che implementa gli algoritmi seguenti.</span><span class="sxs-lookup"><span data-stu-id="973ff-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="973ff-107">Algoritmi simmetrici</span><span class="sxs-lookup"><span data-stu-id="973ff-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="973ff-108">Algoritmi asimmetrici</span><span class="sxs-lookup"><span data-stu-id="973ff-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="973ff-109">Algoritmi di hashing</span><span class="sxs-lookup"><span data-stu-id="973ff-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="973ff-110">Algoritmi di scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="973ff-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="973ff-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="973ff-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="973ff-112">Algoritmi simmetrici</span><span class="sxs-lookup"><span data-stu-id="973ff-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="973ff-113">Nome</span><span class="sxs-lookup"><span data-stu-id="973ff-113">Name</span></span>                                   | <span data-ttu-id="973ff-114">Modalità supportate</span><span class="sxs-lookup"><span data-stu-id="973ff-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="973ff-115">Dimensione della chiave in bit (predefinita/min/max)</span><span class="sxs-lookup"><span data-stu-id="973ff-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="973ff-116">Advanced Encryption Standard (AES)</span><span class="sxs-lookup"><span data-stu-id="973ff-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="973ff-117">BCE, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, wrapping della chiave AES, XTS</span><span class="sxs-lookup"><span data-stu-id="973ff-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="973ff-118">**Windows 8:** Viene avviato il supporto per le modalità CFB128 e CMAC.</span><span class="sxs-lookup"><span data-stu-id="973ff-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="973ff-119">**Windows 10:** Viene avviato il supporto per la modalità XTS-AES.</span><span class="sxs-lookup"><span data-stu-id="973ff-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="973ff-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="973ff-120">128/192/256</span></span>                        |
| <span data-ttu-id="973ff-121">Data Encryption Standard (DES)</span><span class="sxs-lookup"><span data-stu-id="973ff-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="973ff-122">BCE, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="973ff-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="973ff-123">**Windows 8:** Viene avviato il supporto per la modalità CFB64.</span><span class="sxs-lookup"><span data-stu-id="973ff-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="973ff-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="973ff-124">56/56/56</span></span>                           |
| <span data-ttu-id="973ff-125">Data Encryption Standard XORed (DESX)</span><span class="sxs-lookup"><span data-stu-id="973ff-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="973ff-126">BCE, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="973ff-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="973ff-127">**Windows 8:** Viene avviato il supporto per la modalità CFB64.</span><span class="sxs-lookup"><span data-stu-id="973ff-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="973ff-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="973ff-128">192/192/192</span></span>                        |
| <span data-ttu-id="973ff-129">3DES (Triple Data Encryption Standard)</span><span class="sxs-lookup"><span data-stu-id="973ff-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="973ff-130">BCE, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="973ff-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="973ff-131">**Windows 8:** Viene avviato il supporto per la modalità CFB64.</span><span class="sxs-lookup"><span data-stu-id="973ff-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="973ff-132">112/168</span><span class="sxs-lookup"><span data-stu-id="973ff-132">112/168</span></span>                            |
| <span data-ttu-id="973ff-133">RSA Data Security 2 (RC2)</span><span class="sxs-lookup"><span data-stu-id="973ff-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="973ff-134">Sono supportate le modalità BCE, CBC, CFB8 e CFB64.</span><span class="sxs-lookup"><span data-stu-id="973ff-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="973ff-135">**Windows 8:** Viene avviato il supporto per la modalità CFB64.</span><span class="sxs-lookup"><span data-stu-id="973ff-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="973ff-136">da 16 a 128 in incrementi di 8 bit</span><span class="sxs-lookup"><span data-stu-id="973ff-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="973ff-137">RSA Data Security 4 (RC4)</span><span class="sxs-lookup"><span data-stu-id="973ff-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="973ff-138">da 8 a 512, in incrementi a 8 bit</span><span class="sxs-lookup"><span data-stu-id="973ff-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="973ff-139">Algoritmi asimmetrici</span><span class="sxs-lookup"><span data-stu-id="973ff-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="973ff-140">Nome</span><span class="sxs-lookup"><span data-stu-id="973ff-140">Name</span></span>                              | <span data-ttu-id="973ff-141">Note</span><span class="sxs-lookup"><span data-stu-id="973ff-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="973ff-142">Dimensione della chiave in bit (predefinita/min/max)</span><span class="sxs-lookup"><span data-stu-id="973ff-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="973ff-143">Algoritmo di firma digitale (DSA)</span><span class="sxs-lookup"><span data-stu-id="973ff-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="973ff-144">L'implementazione è conforme a FIPS 186-3 per le dimensioni delle chiavi comprese tra 1024 e 3072 bit.</span><span class="sxs-lookup"><span data-stu-id="973ff-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="973ff-145">L'implementazione è conforme a FIPS 186-2 per le dimensioni delle chiavi da 512 a 1024 bit.</span><span class="sxs-lookup"><span data-stu-id="973ff-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="973ff-146">da 512 a 3072, in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="973ff-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="973ff-147">**Windows 8:** Viene avviato il supporto per la chiave a 3072 bit.</span><span class="sxs-lookup"><span data-stu-id="973ff-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="973ff-148">RSA</span><span class="sxs-lookup"><span data-stu-id="973ff-148">RSA</span></span>                               | <span data-ttu-id="973ff-149">Include algoritmi RSA che usano la codifica o la spaziatura interna PKCS1, Optimal Encryption Encryption Padding (OAEP) o la spaziatura in testo non crittografato (PSS Signature Scheme)</span><span class="sxs-lookup"><span data-stu-id="973ff-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="973ff-150">da 512 a 16384, in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="973ff-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="973ff-151">Algoritmi di hashing</span><span class="sxs-lookup"><span data-stu-id="973ff-151">Hashing Algorithms</span></span>



| <span data-ttu-id="973ff-152">Nome</span><span class="sxs-lookup"><span data-stu-id="973ff-152">Name</span></span>                               | <span data-ttu-id="973ff-153">Note</span><span class="sxs-lookup"><span data-stu-id="973ff-153">Notes</span></span>               | <span data-ttu-id="973ff-154">Dimensione della chiave in bit (predefinita/min/max)</span><span class="sxs-lookup"><span data-stu-id="973ff-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="973ff-155">Secure Hash Algorithm 1 (SHA1)</span><span class="sxs-lookup"><span data-stu-id="973ff-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="973ff-156">Include HmacSha1</span><span class="sxs-lookup"><span data-stu-id="973ff-156">Includes HmacSha1</span></span>   | <span data-ttu-id="973ff-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="973ff-157">160/160/160</span></span>                        |
| <span data-ttu-id="973ff-158">Algoritmo Secure Hash Algorithm 256 (SHA256)</span><span class="sxs-lookup"><span data-stu-id="973ff-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="973ff-159">Include HmacSha256</span><span class="sxs-lookup"><span data-stu-id="973ff-159">Includes HmacSha256</span></span> | <span data-ttu-id="973ff-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="973ff-160">256/256/256</span></span>                        |
| <span data-ttu-id="973ff-161">Algoritmo Secure Hash Algorithm 384 (SHA384)</span><span class="sxs-lookup"><span data-stu-id="973ff-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="973ff-162">Include HmacSha384</span><span class="sxs-lookup"><span data-stu-id="973ff-162">Includes HmacSha384</span></span> | <span data-ttu-id="973ff-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="973ff-163">384/384/384</span></span>                        |
| <span data-ttu-id="973ff-164">Algoritmo Secure Hash Algorithm 512 (SHA512)</span><span class="sxs-lookup"><span data-stu-id="973ff-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="973ff-165">Include HmacSha512</span><span class="sxs-lookup"><span data-stu-id="973ff-165">Includes HmacSha512</span></span> | <span data-ttu-id="973ff-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="973ff-166">512/512/512</span></span>                        |
| <span data-ttu-id="973ff-167">Messaggio digest 2 (MD2)</span><span class="sxs-lookup"><span data-stu-id="973ff-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="973ff-168">Include HmacMd2</span><span class="sxs-lookup"><span data-stu-id="973ff-168">Includes HmacMd2</span></span>    | <span data-ttu-id="973ff-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="973ff-169">128/128/128</span></span>                        |
| <span data-ttu-id="973ff-170">Digest del messaggio 4 (MD4)</span><span class="sxs-lookup"><span data-stu-id="973ff-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="973ff-171">Include HmacMd4</span><span class="sxs-lookup"><span data-stu-id="973ff-171">Includes HmacMd4</span></span>    | <span data-ttu-id="973ff-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="973ff-172">128/128/128</span></span>                        |
| <span data-ttu-id="973ff-173">Digest del messaggio 5 (MD5)</span><span class="sxs-lookup"><span data-stu-id="973ff-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="973ff-174">Include HmacMd5</span><span class="sxs-lookup"><span data-stu-id="973ff-174">Includes HmacMd5</span></span>    | <span data-ttu-id="973ff-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="973ff-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="973ff-176">Algoritmi di scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="973ff-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="973ff-177">Nome algoritmo</span><span class="sxs-lookup"><span data-stu-id="973ff-177">Algorithm name</span></span></th>
<th><span data-ttu-id="973ff-178">Note</span><span class="sxs-lookup"><span data-stu-id="973ff-178">Notes</span></span></th>
<th><span data-ttu-id="973ff-179">Dimensione della chiave in bit (predefinita/min/max)</span><span class="sxs-lookup"><span data-stu-id="973ff-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="973ff-180">Algoritmo di scambio delle chiavi Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="973ff-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="973ff-181">da 512 a 4096, in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="973ff-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="973ff-182">Diffie-Hellman a curva ellittica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="973ff-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="973ff-183">Include le curve che usano le chiavi pubbliche 256, 384 e 521 bit, come specificato in SP800-56A.</span><span class="sxs-lookup"><span data-stu-id="973ff-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="973ff-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="973ff-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="973ff-185">Algoritmo di firma digitale a curva ellittica (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="973ff-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="973ff-186">Include le curve che usano le chiavi pubbliche 256, 384 e 521 bit, come specificato in FIPS 186-3.</span><span class="sxs-lookup"><span data-stu-id="973ff-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="973ff-187">Per visualizzare tutte le curve ellittiche denominate, utilizzare <strong>certutil displayEccCurve</strong>.</span><span class="sxs-lookup"><span data-stu-id="973ff-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="973ff-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="973ff-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="973ff-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="973ff-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="973ff-190">**Identificatori dell'algoritmo CNG**</span><span class="sxs-lookup"><span data-stu-id="973ff-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="973ff-191">Funzioni primitive di crittografia CNG</span><span class="sxs-lookup"><span data-stu-id="973ff-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="973ff-192">Informazioni sui provider di crittografia</span><span class="sxs-lookup"><span data-stu-id="973ff-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

