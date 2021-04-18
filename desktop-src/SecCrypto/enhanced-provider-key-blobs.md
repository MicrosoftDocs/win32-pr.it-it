---
description: Il provider di base, il provider sicuro e il provider migliorato utilizzano gli stessi BLOB di chiavi.
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: BLOB chiave provider avanzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f693fd469a1df2e76078e61bb69c90ea5d5041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316178"
---
# <a name="enhanced-provider-key-blobs"></a><span data-ttu-id="45d9f-103">BLOB chiave provider avanzati</span><span class="sxs-lookup"><span data-stu-id="45d9f-103">Enhanced Provider Key BLOBs</span></span>

<span data-ttu-id="45d9f-104">Il provider di base, il provider sicuro e il provider migliorato utilizzano gli stessi [*BLOB di chiavi*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="45d9f-104">The Base Provider, Strong Provider, and Enhanced Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="45d9f-105">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="45d9f-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="45d9f-106">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="45d9f-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="45d9f-107">BLOB di chiavi semplici</span><span class="sxs-lookup"><span data-stu-id="45d9f-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="45d9f-108">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="45d9f-108">Public Key BLOBs</span></span>

<span data-ttu-id="45d9f-109">I [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per archiviare le [*chiavi pubbliche*](../secgloss/p-gly.md) all'esterno di un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="45d9f-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="45d9f-110">I BLOB di chiavi pubbliche del provider esteso hanno il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="45d9f-110">Extended provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="45d9f-111">Nella tabella seguente viene descritto ogni componente di chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="45d9f-111">The following table describes each public key component.</span></span> <span data-ttu-id="45d9f-112">Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="45d9f-113">Campo</span><span class="sxs-lookup"><span data-stu-id="45d9f-113">Field</span></span>          | <span data-ttu-id="45d9f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45d9f-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d9f-115">modulo</span><span class="sxs-lookup"><span data-stu-id="45d9f-115">modulus</span></span>        | <span data-ttu-id="45d9f-116">I dati del modulo della chiave pubblica si trovano immediatamente dopo la struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="45d9f-117">Le dimensioni di questi dati variano a seconda delle dimensioni della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="45d9f-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="45d9f-118">Il numero di byte può essere determinato dividendo il valore del campo **RSAPUBKEY bitlen** di otto.</span><span class="sxs-lookup"><span data-stu-id="45d9f-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="45d9f-119">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="45d9f-119">publickeystruc</span></span> | <span data-ttu-id="45d9f-120">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="45d9f-121">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="45d9f-121">rsapubkey</span></span>      | <span data-ttu-id="45d9f-122">Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="45d9f-123">Il membro **Magic** deve essere impostato su 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="45d9f-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="45d9f-124">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa1.</span><span class="sxs-lookup"><span data-stu-id="45d9f-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="45d9f-125">I BLOB di chiavi pubbliche non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="45d9f-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="45d9f-126">Contengono chiavi pubbliche in formato [*testo non crittografato*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="45d9f-127">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="45d9f-127">Private Key BLOBs</span></span>

<span data-ttu-id="45d9f-128">I [*BLOB di chiavi private*](../secgloss/p-gly.md), digitare **PRIVATEKEYBLOB**, vengono usati per archiviare [*chiavi private*](../secgloss/p-gly.md) all'esterno di un CSP.</span><span class="sxs-lookup"><span data-stu-id="45d9f-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="45d9f-129">I BLOB di chiavi private del provider esteso hanno il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="45d9f-129">Extended provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="45d9f-130">Nella tabella seguente viene descritto il componente BLOB della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="45d9f-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="45d9f-131">Questi campi corrispondono ai campi descritti nella sezione 7,2 di [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con differenze minime.</span><span class="sxs-lookup"><span data-stu-id="45d9f-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="45d9f-132">Campo</span><span class="sxs-lookup"><span data-stu-id="45d9f-132">Field</span></span>           | <span data-ttu-id="45d9f-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45d9f-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d9f-134">coefficiente</span><span class="sxs-lookup"><span data-stu-id="45d9f-134">coefficient</span></span>     | <span data-ttu-id="45d9f-135">Coefficiente.</span><span class="sxs-lookup"><span data-stu-id="45d9f-135">Coefficient.</span></span> <span data-ttu-id="45d9f-136">Il valore numerico è (inverso di q) mod p.</span><span class="sxs-lookup"><span data-stu-id="45d9f-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="45d9f-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="45d9f-137">exponent1</span></span>       | <span data-ttu-id="45d9f-138">Esponente 1.</span><span class="sxs-lookup"><span data-stu-id="45d9f-138">Exponent 1.</span></span> <span data-ttu-id="45d9f-139">Il valore numerico è d mod (p-1).</span><span class="sxs-lookup"><span data-stu-id="45d9f-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="45d9f-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="45d9f-140">exponent2</span></span>       | <span data-ttu-id="45d9f-141">Esponente 2.</span><span class="sxs-lookup"><span data-stu-id="45d9f-141">Exponent 2.</span></span> <span data-ttu-id="45d9f-142">Il valore numerico è d mod (q-1).</span><span class="sxs-lookup"><span data-stu-id="45d9f-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="45d9f-143">Modulus</span><span class="sxs-lookup"><span data-stu-id="45d9f-143">Modulus</span></span>         | <span data-ttu-id="45d9f-144">Modulo.</span><span class="sxs-lookup"><span data-stu-id="45d9f-144">The modulus.</span></span> <span data-ttu-id="45d9f-145">Il valore è *Prime1*×*prime2* ed è spesso noto come n.</span><span class="sxs-lookup"><span data-stu-id="45d9f-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="45d9f-146">prime1</span><span class="sxs-lookup"><span data-stu-id="45d9f-146">prime1</span></span>          | <span data-ttu-id="45d9f-147">Numero primo 1, spesso noto come p.</span><span class="sxs-lookup"><span data-stu-id="45d9f-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="45d9f-148">prime2</span><span class="sxs-lookup"><span data-stu-id="45d9f-148">prime2</span></span>          | <span data-ttu-id="45d9f-149">Numero primo 2, spesso noto come q.</span><span class="sxs-lookup"><span data-stu-id="45d9f-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="45d9f-150">privateExponent</span><span class="sxs-lookup"><span data-stu-id="45d9f-150">privateExponent</span></span> | <span data-ttu-id="45d9f-151">Esponente privato, spesso noto come d.</span><span class="sxs-lookup"><span data-stu-id="45d9f-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="45d9f-152">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="45d9f-152">publickeystruc</span></span>  | <span data-ttu-id="45d9f-153">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="45d9f-154">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="45d9f-154">rsapubkey</span></span>       | <span data-ttu-id="45d9f-155">Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="45d9f-156">Il membro **Magic** deve essere impostato su 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="45d9f-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="45d9f-157">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa2.</span><span class="sxs-lookup"><span data-stu-id="45d9f-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="45d9f-158">I BLOB di chiavi private non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="45d9f-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="45d9f-159">Contengono chiavi private in formato testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="45d9f-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="45d9f-160">Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave.</span><span class="sxs-lookup"><span data-stu-id="45d9f-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="45d9f-161">**PRIVATEKEYBLOB** viene crittografato se il parametro *hExpKey* contiene un handle valido per una chiave di sessione.</span><span class="sxs-lookup"><span data-stu-id="45d9f-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="45d9f-162">Tutto tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata.</span><span class="sxs-lookup"><span data-stu-id="45d9f-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="45d9f-163">L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="45d9f-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="45d9f-164">L'applicazione deve gestire e archiviare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="45d9f-164">The application must manage and store this information.</span></span> <span data-ttu-id="45d9f-165">Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.</span><span class="sxs-lookup"><span data-stu-id="45d9f-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="45d9f-166">È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.</span><span class="sxs-lookup"><span data-stu-id="45d9f-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="45d9f-167">BLOB di chiavi semplici</span><span class="sxs-lookup"><span data-stu-id="45d9f-167">Simple Key BLOBs</span></span>

<span data-ttu-id="45d9f-168">I [*BLOB di chiavi semplici*](../secgloss/s-gly.md), digitare **SIMPLEBLOB**, vengono usati per archiviare e trasportare chiavi di sessione all'esterno di un CSP.</span><span class="sxs-lookup"><span data-stu-id="45d9f-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="45d9f-169">I BLOB di chiavi semplici del provider esteso sono sempre crittografati con una [*chiave pubblica di scambio delle chiavi*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="45d9f-169">Extended provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="45d9f-170">Il membro **pbData** di **SIMPLEBLOB** è una sequenza di byte nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="45d9f-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="45d9f-171">Nella tabella seguente viene descritto ogni componente del membro **pbData** di **SIMPLEBLOB**.</span><span class="sxs-lookup"><span data-stu-id="45d9f-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="45d9f-172">Campo</span><span class="sxs-lookup"><span data-stu-id="45d9f-172">Field</span></span>          | <span data-ttu-id="45d9f-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45d9f-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d9f-174">algido</span><span class="sxs-lookup"><span data-stu-id="45d9f-174">algid</span></span>          | <span data-ttu-id="45d9f-175">Struttura [**di \_ ID ALG**](alg-id.md) che specifica l'algoritmo di crittografia utilizzato per crittografare i dati della chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="45d9f-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="45d9f-176">Questo ha in genere il valore CALG \_ RSA \_ KEYX, che indica che i dati della chiave della sessione sono stati crittografati con una chiave pubblica di scambio delle chiavi usando l' [*algoritmo di chiave pubblica RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="45d9f-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="45d9f-177">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="45d9f-177">encryptedkey</span></span>   | <span data-ttu-id="45d9f-178">Sequenza di **byte** che rappresenta i dati della chiave della sessione crittografata sotto forma di un \# blocco di crittografia PKCS 1, Type 2.</span><span class="sxs-lookup"><span data-stu-id="45d9f-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="45d9f-179">Per informazioni su questo formato dati, vedere la pagina relativa a Public Key Cryptography Standards (PKCS) \# 1, pubblicata da RSA Data Security, Inc. Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="45d9f-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="45d9f-180">Ad esempio, le chiavi pubbliche generate dal provider di base Microsoft RSA possono avere una lunghezza di 512 bit (64 byte), quindi anche i dati della chiave della sessione crittografata sono sempre 512 bit (64 byte).</span><span class="sxs-lookup"><span data-stu-id="45d9f-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="45d9f-181">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="45d9f-181">publickeystruc</span></span> | <span data-ttu-id="45d9f-182">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="45d9f-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

<span data-ttu-id="45d9f-183">Per informazioni sui BLOB di chiavi del provider di base e del provider esteso, vedere [BLOB chiave](base-provider-key-blobs.md)del provider di base.</span><span class="sxs-lookup"><span data-stu-id="45d9f-183">For information about the Base Provider and Extended Provider key BLOBs, see [Base Provider Key BLOBs](base-provider-key-blobs.md).</span></span>

 

 
