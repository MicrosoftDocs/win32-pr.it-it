---
description: I BLOB vengono utilizzati con il provider RSA/SChannel per esportare chiavi da e importare chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOB di chiavi RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879474"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="ec7c4-103">BLOB di chiavi RSA/SChannel</span><span class="sxs-lookup"><span data-stu-id="ec7c4-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="ec7c4-104">I [*BLOB*](../secgloss/b-gly.md) vengono utilizzati con [](../secgloss/r-gly.md)il / provider [*Schannel*](../secgloss/s-gly.md) RSA per esportare chiavi da e importare chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="ec7c4-105">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="ec7c4-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="ec7c4-106">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="ec7c4-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="ec7c4-107">BLOB di chiavi semplici</span><span class="sxs-lookup"><span data-stu-id="ec7c4-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="ec7c4-108">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="ec7c4-108">Public Key BLOBs</span></span>

<span data-ttu-id="ec7c4-109">I [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per archiviare le [*chiavi pubbliche*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="ec7c4-110">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="ec7c4-111">Nella tabella seguente viene descritto ogni componente di chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-111">The following table describes each public key component.</span></span> <span data-ttu-id="ec7c4-112">Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="ec7c4-113">Campo</span><span class="sxs-lookup"><span data-stu-id="ec7c4-113">Field</span></span>          | <span data-ttu-id="ec7c4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec7c4-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7c4-115">modulo</span><span class="sxs-lookup"><span data-stu-id="ec7c4-115">modulus</span></span>        | <span data-ttu-id="ec7c4-116">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-116">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-117">I dati del modulo della chiave pubblica si trovano immediatamente dopo la struttura **RSAPUBKEY** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="ec7c4-118">La lunghezza di questi dati varia a seconda della lunghezza della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="ec7c4-119">Il numero di byte può essere determinato dividendo il valore del membro **bitlen** di **RSAPUBKEY** di otto.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="ec7c4-120">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="ec7c4-120">publickeystruc</span></span> | <span data-ttu-id="ec7c4-121">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="ec7c4-122">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="ec7c4-122">rsapubkey</span></span>      | <span data-ttu-id="ec7c4-123">Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="ec7c4-124">Il membro **Magic** deve essere impostato su 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="ec7c4-125">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa1.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="ec7c4-126">I BLOB di chiavi pubbliche non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="ec7c4-127">Contengono chiavi pubbliche in formato [*testo non crittografato*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="ec7c4-128">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="ec7c4-128">Private Key BLOBs</span></span>

<span data-ttu-id="ec7c4-129">I [*BLOB di chiavi private*](../secgloss/p-gly.md), digitare **PRIVATEKEYBLOB**, vengono usati per archiviare [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="ec7c4-130">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="ec7c4-131">Se il [*BLOB della chiave*](../secgloss/k-gly.md) è crittografato, tutti gli elementi tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB vengono crittografati.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="ec7c4-132">L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="ec7c4-133">È responsabilità dell'applicazione gestire queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="ec7c4-134">Nella tabella seguente viene descritto ogni componente BLOB della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="ec7c4-135">Questi campi corrispondono ai campi descritti nella sezione 7,2 di [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con differenze minime.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="ec7c4-136">Campo</span><span class="sxs-lookup"><span data-stu-id="ec7c4-136">Field</span></span>           | <span data-ttu-id="ec7c4-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec7c4-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7c4-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="ec7c4-138">exponent1</span></span>       | <span data-ttu-id="ec7c4-139">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-139">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-140">Primo esponente.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-140">The first exponent.</span></span> <span data-ttu-id="ec7c4-141">Il valore numerico è d mod (p-1).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="ec7c4-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="ec7c4-142">exponent2</span></span>       | <span data-ttu-id="ec7c4-143">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-143">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-144">Secondo esponente.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-144">The second exponent.</span></span> <span data-ttu-id="ec7c4-145">Il valore numerico è d mod (q-1).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="ec7c4-146">coefficiente</span><span class="sxs-lookup"><span data-stu-id="ec7c4-146">coefficient</span></span>     | <span data-ttu-id="ec7c4-147">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-147">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-148">Coefficiente.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-148">Coefficient.</span></span> <span data-ttu-id="ec7c4-149">Il valore numerico è (inverso di q) mod p.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="ec7c4-150">Modulus</span><span class="sxs-lookup"><span data-stu-id="ec7c4-150">Modulus</span></span>         | <span data-ttu-id="ec7c4-151">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-151">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-152">Modulo.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-152">The modulus.</span></span> <span data-ttu-id="ec7c4-153">Contiene una stringa che contiene *Prime1* \* *prime2*.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="ec7c4-154">Spesso è noto come n.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="ec7c4-155">prime1</span><span class="sxs-lookup"><span data-stu-id="ec7c4-155">prime1</span></span>          | <span data-ttu-id="ec7c4-156">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-156">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-157">Numero primo 1, spesso noto come p.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="ec7c4-158">prime2</span><span class="sxs-lookup"><span data-stu-id="ec7c4-158">prime2</span></span>          | <span data-ttu-id="ec7c4-159">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-159">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-160">Numero primo 2, spesso noto come q.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="ec7c4-161">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="ec7c4-161">publickeystruc</span></span>  | <span data-ttu-id="ec7c4-162">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="ec7c4-163">privateExponent</span><span class="sxs-lookup"><span data-stu-id="ec7c4-163">privateExponent</span></span> | <span data-ttu-id="ec7c4-164">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-164">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-165">Esponente privato, spesso noto come d.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="ec7c4-166">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="ec7c4-166">rsapubkey</span></span>       | <span data-ttu-id="ec7c4-167">Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="ec7c4-168">Il membro **Magic** deve essere impostato su 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="ec7c4-169">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa2.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="ec7c4-170">I BLOB di chiavi private non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="ec7c4-171">Contengono chiavi private in formato testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="ec7c4-172">Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="ec7c4-173">**PRIVATEKEYBLOB** viene crittografato se il parametro *hExpKey* contiene un handle valido per una chiave di sessione.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="ec7c4-174">Tutto tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="ec7c4-175">L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="ec7c4-176">L'applicazione deve gestire e archiviare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-176">The application must manage and store this information.</span></span> <span data-ttu-id="ec7c4-177">Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="ec7c4-178">È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="ec7c4-179">BLOB di chiavi semplici</span><span class="sxs-lookup"><span data-stu-id="ec7c4-179">Simple Key BLOBs</span></span>

<span data-ttu-id="ec7c4-180">I [*BLOB di chiavi semplici*](../secgloss/s-gly.md), digitare **SIMPLEBLOB**, vengono usati per archiviare e trasportare le chiavi della sessione.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="ec7c4-181">Sono sempre crittografati con una chiave [*pubblica di scambio delle chiavi*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="ec7c4-182">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="ec7c4-183">Nella tabella seguente vengono descritti i singoli componenti BLOB semplici.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="ec7c4-184">Campo</span><span class="sxs-lookup"><span data-stu-id="ec7c4-184">Field</span></span>          | <span data-ttu-id="ec7c4-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec7c4-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7c4-186">algido</span><span class="sxs-lookup"><span data-stu-id="ec7c4-186">algid</span></span>          | <span data-ttu-id="ec7c4-187">Struttura [**di \_ ID ALG**](alg-id.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="ec7c4-188">In genere viene specificato l' \_ algoritmo CALG RSA \_ KEYX, che indica che i dati della chiave della sessione sono stati crittografati con una chiave pubblica di scambio delle chiavi, usando l' [*algoritmo di chiave pubblica RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ec7c4-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="ec7c4-189">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="ec7c4-189">encryptedkey</span></span>   | <span data-ttu-id="ec7c4-190">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-190">A **BYTE** sequence.</span></span> <span data-ttu-id="ec7c4-191">I dati della chiave della sessione crittografata hanno il formato di un \# blocco di crittografia PKCS 1, Type 2.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="ec7c4-192">Per informazioni su questo formato dati, vedere la pagina relativa a Public Key Cryptography Standards (PKCS), pubblicata da RSA Data Security, Inc.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="ec7c4-193">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="ec7c4-193">publickeystruc</span></span> | <span data-ttu-id="ec7c4-194">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="ec7c4-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="ec7c4-195">Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="ec7c4-196">Ad esempio, le chiavi pubbliche generate dal provider di crittografia di base Microsoft sono sempre di 512 bit (64 byte), quindi anche i dati della chiave della sessione crittografata sono sempre 64 byte.</span><span class="sxs-lookup"><span data-stu-id="ec7c4-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 
