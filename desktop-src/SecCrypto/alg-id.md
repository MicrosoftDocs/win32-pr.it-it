---
description: Specifica un identificatore di algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319368"
---
# <a name="alg_id"></a><span data-ttu-id="755b6-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="755b6-103">ALG_ID</span></span>

<span data-ttu-id="755b6-104">Il tipo di dati **ALG_ID** specifica un identificatore di algoritmo.</span><span class="sxs-lookup"><span data-stu-id="755b6-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="755b6-105">I parametri di questo tipo di dati vengono passati alla maggior parte delle funzioni in CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="755b6-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="755b6-106">Nella tabella seguente sono elencati gli identificatori degli algoritmi attualmente definiti.</span><span class="sxs-lookup"><span data-stu-id="755b6-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="755b6-107">Gli autori di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) personalizzati possono definire nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="755b6-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="755b6-108">Inoltre, le **ALG_ID** utilizzate da DSN personalizzati per le specifiche chiave **AT_KEYEXCHANGE** e **AT_SIGNATURE** sono dipendenti dal provider.</span><span class="sxs-lookup"><span data-stu-id="755b6-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="755b6-109">I mapping correnti seguono la tabella.</span><span class="sxs-lookup"><span data-stu-id="755b6-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="755b6-110">Identificatore</span><span class="sxs-lookup"><span data-stu-id="755b6-110">Identifier</span></span></th>
<th><span data-ttu-id="755b6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="755b6-111">Value</span></span></th>
<th><span data-ttu-id="755b6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="755b6-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="755b6-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="755b6-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="755b6-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="755b6-114">0x00006603</span></span></td>
<td><span data-ttu-id="755b6-115">Algoritmo di crittografia <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> .</span><span class="sxs-lookup"><span data-stu-id="755b6-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="755b6-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="755b6-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="755b6-117">0x00006609</span></span></td>
<td><span data-ttu-id="755b6-118">Crittografia <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> a due chiavi con lunghezza chiave effettiva uguale a 112 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="755b6-119">CALG_AES</span></span></td>
<td><span data-ttu-id="755b6-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="755b6-120">0x00006611</span></span></td>
<td><span data-ttu-id="755b6-121">Advanced Encryption Standard (AES).</span><span class="sxs-lookup"><span data-stu-id="755b6-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="755b6-122">Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="755b6-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="755b6-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="755b6-124">0x0000660e</span></span></td>
<td><span data-ttu-id="755b6-125">AES a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-125">128 bit AES.</span></span> <span data-ttu-id="755b6-126">Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="755b6-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="755b6-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="755b6-128">0x0000660f</span></span></td>
<td><span data-ttu-id="755b6-129">AES a 192 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-129">192 bit AES.</span></span> <span data-ttu-id="755b6-130">Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="755b6-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="755b6-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="755b6-132">0x00006610</span></span></td>
<td><span data-ttu-id="755b6-133">AES a 256 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-133">256 bit AES.</span></span> <span data-ttu-id="755b6-134">Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="755b6-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="755b6-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="755b6-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="755b6-137">Identificatore di algoritmo temporaneo per gli handle delle chiavi concordate Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="755b6-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="755b6-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="755b6-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="755b6-139">0x0000660c</span></span></td>
<td><span data-ttu-id="755b6-140">Algoritmo per la creazione di una chiave DES a 40 bit con bit di parità e bit di chiave zero per ottenere la lunghezza della chiave 64 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="755b6-141">Questo algoritmo è supportato dal <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="755b6-142">CALG_DES</span></span></td>
<td><span data-ttu-id="755b6-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="755b6-143">0x00006601</span></span></td>
<td><span data-ttu-id="755b6-144">Algoritmo di crittografia DES.</span><span class="sxs-lookup"><span data-stu-id="755b6-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="755b6-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="755b6-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="755b6-146">0x00006604</span></span></td>
<td><span data-ttu-id="755b6-147">Algoritmo di crittografia DESX.</span><span class="sxs-lookup"><span data-stu-id="755b6-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="755b6-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="755b6-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="755b6-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="755b6-150">Diffie-Hellman algoritmo di scambio di chiave temporaneo.</span><span class="sxs-lookup"><span data-stu-id="755b6-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="755b6-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="755b6-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="755b6-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="755b6-153">Diffie-Hellman archiviare e inviare l'algoritmo di scambio di chiave.</span><span class="sxs-lookup"><span data-stu-id="755b6-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="755b6-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="755b6-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="755b6-155">0x00002200</span></span></td>
<td><span data-ttu-id="755b6-156">Algoritmo di firma della <a href="/windows/desktop/SecGloss/p-gly"><em>chiave pubblica</em></a> DSA.</span><span class="sxs-lookup"><span data-stu-id="755b6-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="755b6-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="755b6-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="755b6-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="755b6-159">Curva ellittica Diffie-Hellman algoritmo di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="755b6-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="755b6-160">Questo algoritmo è supportato solo tramite l' <a href="/windows/desktop/SecCNG/cng-portal">API di crittografia: Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="755b6-161"><strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="755b6-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="755b6-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="755b6-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="755b6-164">Curva ellittica temporanea Diffie-Hellman algoritmo di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="755b6-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="755b6-165">Questo algoritmo è supportato solo tramite l' <a href="/windows/desktop/SecCNG/cng-portal">API di crittografia: Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="755b6-166"><strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="755b6-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="755b6-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="755b6-168">0x00002203</span></span></td>
<td><span data-ttu-id="755b6-169">Algoritmo di firma digitale a curva ellittica.</span><span class="sxs-lookup"><span data-stu-id="755b6-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="755b6-170">Questo algoritmo è supportato solo tramite l' <a href="/windows/desktop/SecCNG/cng-portal">API di crittografia: Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="755b6-171"><strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="755b6-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="755b6-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="755b6-173">0x0000a001</span></span></td>
<td><span data-ttu-id="755b6-174">Algoritmo di scambio delle chiavi Menezes, qu e Vanstone (MQV) a curva ellittica.</span><span class="sxs-lookup"><span data-stu-id="755b6-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="755b6-175">Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="755b6-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="755b6-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="755b6-177">0x0000800b</span></span></td>
<td><span data-ttu-id="755b6-178">Algoritmo di hashing della funzione unidirezionale.</span><span class="sxs-lookup"><span data-stu-id="755b6-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="755b6-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="755b6-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="755b6-180">0x0000a003</span></span></td>
<td><span data-ttu-id="755b6-181">Algoritmo di hash MD5 Hughes.</span><span class="sxs-lookup"><span data-stu-id="755b6-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="755b6-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="755b6-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="755b6-183">0x00008009</span></span></td>
<td><span data-ttu-id="755b6-184">Algoritmo hash con chiave HMAC.</span><span class="sxs-lookup"><span data-stu-id="755b6-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="755b6-185">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="755b6-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="755b6-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="755b6-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="755b6-188">Algoritmo di scambio delle chiavi di KEA (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="755b6-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="755b6-189">Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="755b6-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="755b6-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="755b6-191">0x00008005</span></span></td>
<td><span data-ttu-id="755b6-192">Algoritmo hash con chiave <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> .</span><span class="sxs-lookup"><span data-stu-id="755b6-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="755b6-193">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="755b6-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="755b6-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="755b6-195">0x00008001</span></span></td>
<td><span data-ttu-id="755b6-196">Algoritmo di hash MD2.</span><span class="sxs-lookup"><span data-stu-id="755b6-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="755b6-197">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="755b6-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="755b6-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="755b6-199">0x00008002</span></span></td>
<td><span data-ttu-id="755b6-200">Algoritmo di hash MD4.</span><span class="sxs-lookup"><span data-stu-id="755b6-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="755b6-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="755b6-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="755b6-202">0x00008003</span></span></td>
<td><span data-ttu-id="755b6-203">Algoritmo di hash MD5.</span><span class="sxs-lookup"><span data-stu-id="755b6-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="755b6-204">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="755b6-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="755b6-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="755b6-206">0x00002000</span></span></td>
<td><span data-ttu-id="755b6-207">Nessun algoritmo di firma.</span><span class="sxs-lookup"><span data-stu-id="755b6-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="755b6-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="755b6-209">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="755b6-209">0xffffffff</span></span></td>
<td><span data-ttu-id="755b6-210">L'algoritmo viene implementato solo in CNG.</span><span class="sxs-lookup"><span data-stu-id="755b6-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="755b6-211">La macro, IS_SPECIAL_OID_INFO_ALGID, può essere utilizzata per determinare se un algoritmo di crittografia è supportato solo tramite le funzioni CNG.</span><span class="sxs-lookup"><span data-stu-id="755b6-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="755b6-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="755b6-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="755b6-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="755b6-214">L'algoritmo viene definito nei parametri codificati.</span><span class="sxs-lookup"><span data-stu-id="755b6-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="755b6-215">L'algoritmo è supportato solo mediante CNG.</span><span class="sxs-lookup"><span data-stu-id="755b6-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="755b6-216">La macro, IS_SPECIAL_OID_INFO_ALGID, può essere utilizzata per determinare se un algoritmo di crittografia è supportato solo tramite le funzioni CNG.</span><span class="sxs-lookup"><span data-stu-id="755b6-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="755b6-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="755b6-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="755b6-218">0x00004c04</span></span></td>
<td><span data-ttu-id="755b6-219">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-220">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="755b6-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="755b6-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="755b6-222">0x00006602</span></span></td>
<td><span data-ttu-id="755b6-223">Algoritmo di crittografia a blocchi RC2.</span><span class="sxs-lookup"><span data-stu-id="755b6-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="755b6-224">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="755b6-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="755b6-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="755b6-226">0x00006801</span></span></td>
<td><span data-ttu-id="755b6-227">Algoritmo di crittografia del flusso RC4.</span><span class="sxs-lookup"><span data-stu-id="755b6-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="755b6-228">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="755b6-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="755b6-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="755b6-230">0x0000660d</span></span></td>
<td><span data-ttu-id="755b6-231">Algoritmo di crittografia a blocchi RC5.</span><span class="sxs-lookup"><span data-stu-id="755b6-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="755b6-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="755b6-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="755b6-233">0x0000a400</span></span></td>
<td><span data-ttu-id="755b6-234">Algoritmo di scambio di chiave pubblica RSA.</span><span class="sxs-lookup"><span data-stu-id="755b6-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="755b6-235">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="755b6-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="755b6-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="755b6-237">0x00002400</span></span></td>
<td><span data-ttu-id="755b6-238">Algoritmo di firma della chiave pubblica RSA.</span><span class="sxs-lookup"><span data-stu-id="755b6-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="755b6-239">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="755b6-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="755b6-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="755b6-241">0x00004c07</span></span></td>
<td><span data-ttu-id="755b6-242">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-243">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="755b6-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="755b6-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="755b6-245">0x00004c03</span></span></td>
<td><span data-ttu-id="755b6-246">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-247">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="755b6-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="755b6-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="755b6-249">0x00004c02</span></span></td>
<td><span data-ttu-id="755b6-250">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-251">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="755b6-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="755b6-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="755b6-253">0x00006802</span></span></td>
<td><span data-ttu-id="755b6-254">Algoritmo di crittografia SEAL.</span><span class="sxs-lookup"><span data-stu-id="755b6-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="755b6-255">Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="755b6-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="755b6-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="755b6-257">0x00008004</span></span></td>
<td><span data-ttu-id="755b6-258">Algoritmo di hash SHA.</span><span class="sxs-lookup"><span data-stu-id="755b6-258">SHA hashing algorithm.</span></span> <span data-ttu-id="755b6-259">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="755b6-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="755b6-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="755b6-261">0x00008004</span></span></td>
<td><span data-ttu-id="755b6-262">Uguale a <strong>CALG_SHA</strong>.</span><span class="sxs-lookup"><span data-stu-id="755b6-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="755b6-263">Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="755b6-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="755b6-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="755b6-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="755b6-265">0x0000800c</span></span></td>
<td><span data-ttu-id="755b6-266">algoritmo di hash SHA a 256 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="755b6-267">Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (prototipo).</span><span class="sxs-lookup"><span data-stu-id="755b6-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="755b6-268"><strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="755b6-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="755b6-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="755b6-270">0x0000800d</span></span></td>
<td><span data-ttu-id="755b6-271">algoritmo di hash SHA a 384 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="755b6-272">Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (prototipo).</span><span class="sxs-lookup"><span data-stu-id="755b6-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="755b6-273"><strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="755b6-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="755b6-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="755b6-275">0x0000800e</span></span></td>
<td><span data-ttu-id="755b6-276">algoritmo di hash SHA a 512 bit.</span><span class="sxs-lookup"><span data-stu-id="755b6-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="755b6-277">Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (prototipo).</span><span class="sxs-lookup"><span data-stu-id="755b6-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="755b6-278"><strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="755b6-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="755b6-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="755b6-280">0x0000660a</span></span></td>
<td><span data-ttu-id="755b6-281">Skipjack Block Encryption Algorithm (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="755b6-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="755b6-282">Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="755b6-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="755b6-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="755b6-284">0x00004c05</span></span></td>
<td><span data-ttu-id="755b6-285">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-286">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="755b6-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="755b6-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="755b6-288">0x00004c01</span></span></td>
<td><span data-ttu-id="755b6-289">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-290">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="755b6-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="755b6-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="755b6-292">0x00008008</span></span></td>
<td><span data-ttu-id="755b6-293">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-294">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="755b6-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="755b6-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="755b6-296">0x0000660b</span></span></td>
<td><span data-ttu-id="755b6-297">TEK (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="755b6-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="755b6-298">Questo algoritmo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="755b6-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="755b6-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="755b6-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="755b6-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="755b6-300">0x00004c06</span></span></td>
<td><span data-ttu-id="755b6-301">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-302">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="755b6-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="755b6-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="755b6-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="755b6-304">0x0000800a</span></span></td>
<td><span data-ttu-id="755b6-305">Utilizzato dal sistema operativo Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="755b6-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="755b6-306">Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="755b6-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="755b6-307">Per [Microsoft Base Cryptographic](microsoft-base-cryptographic-provider.md)provider, [Microsoft Strong Cryptographic](microsoft-strong-cryptographic-provider.md)provider e [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), le **ALG_IDs** utilizzate per le specifiche principali **AT_KEYEXCHANGE** e **AT_SIGNATURE** sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="755b6-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="755b6-308">**CALG_RSA_KEYX** viene utilizzato per **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="755b6-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="755b6-309">**CALG_RSA_SIGN** viene utilizzato per **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="755b6-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="755b6-310">Per [Microsoft Base DSS e Diffie-Hellman provider di crittografia](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), i **ALG_IDs** usati per le specifiche principali **AT_KEYEXCHANGE** e **AT_SIGNATURE** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="755b6-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="755b6-311">**CALG_DH_SF** viene utilizzato per **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="755b6-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="755b6-312">**CALG_DSS_SIGN** viene utilizzato per **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="755b6-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="755b6-313">Requisiti</span><span class="sxs-lookup"><span data-stu-id="755b6-313">Requirements</span></span>



| <span data-ttu-id="755b6-314">Requisito</span><span class="sxs-lookup"><span data-stu-id="755b6-314">Requirement</span></span> | <span data-ttu-id="755b6-315">Valore</span><span class="sxs-lookup"><span data-stu-id="755b6-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="755b6-316">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="755b6-316">Minimum supported client</span></span><br/> | <span data-ttu-id="755b6-317">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="755b6-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="755b6-318">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="755b6-318">Minimum supported server</span></span><br/> | <span data-ttu-id="755b6-319">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="755b6-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="755b6-320">Intestazione</span><span class="sxs-lookup"><span data-stu-id="755b6-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="755b6-321"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="755b6-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755b6-322">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="755b6-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755b6-323">Funzioni di crittografia</span><span class="sxs-lookup"><span data-stu-id="755b6-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="755b6-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="755b6-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="755b6-325">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="755b6-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
