---
description: Usato con il provider Digital Signature Standard (DSS) per esportare chiavi da e importare chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: BLOB di chiavi del provider DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966590"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="145a2-103">BLOB di chiavi del provider DSS</span><span class="sxs-lookup"><span data-stu-id="145a2-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="145a2-104">I [*BLOB*](../secgloss/b-gly.md) vengono utilizzati con il provider [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) per esportare chiavi da e importare chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="145a2-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="145a2-105">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="145a2-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="145a2-106">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="145a2-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="145a2-107">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="145a2-107">Public Key BLOBs</span></span>

<span data-ttu-id="145a2-108">Una [*chiave pubblica*](../secgloss/p-gly.md) DSS viene esportata e importata come BLOB, una sequenza di byte strutturata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="145a2-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="145a2-109">Nella tabella seguente vengono descritti questi componenti.</span><span class="sxs-lookup"><span data-stu-id="145a2-109">The following table describes these components.</span></span> <span data-ttu-id="145a2-110">Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="145a2-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="145a2-111">Campo</span><span class="sxs-lookup"><span data-stu-id="145a2-111">Field</span></span>          | <span data-ttu-id="145a2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="145a2-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="145a2-113">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="145a2-113">dsspubkey</span></span>      | <span data-ttu-id="145a2-114">Struttura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="145a2-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="145a2-115">Il membro **Magic** deve avere un valore 0x31535344.</span><span class="sxs-lookup"><span data-stu-id="145a2-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="145a2-116">Questo numero esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DSS1.</span><span class="sxs-lookup"><span data-stu-id="145a2-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="145a2-117">g</span><span class="sxs-lookup"><span data-stu-id="145a2-117">g</span></span>              | <span data-ttu-id="145a2-118">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-118">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-119">Il generatore, g.</span><span class="sxs-lookup"><span data-stu-id="145a2-119">The generator, g.</span></span> <span data-ttu-id="145a2-120">Deve avere la stessa lunghezza di p.</span><span class="sxs-lookup"><span data-stu-id="145a2-120">Must be the same length as p.</span></span> <span data-ttu-id="145a2-121">Se non ha la stessa lunghezza di p, deve essere riempita con 0x00 byte.</span><span class="sxs-lookup"><span data-stu-id="145a2-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="145a2-122">p</span><span class="sxs-lookup"><span data-stu-id="145a2-122">p</span></span>              | <span data-ttu-id="145a2-123">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-123">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-124">Il modulo principale, p.</span><span class="sxs-lookup"><span data-stu-id="145a2-124">The prime modulus, p.</span></span> <span data-ttu-id="145a2-125">Il bit più significativo del byte più significativo deve essere impostato su uno.</span><span class="sxs-lookup"><span data-stu-id="145a2-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="145a2-126">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="145a2-126">publickeystruc</span></span> | <span data-ttu-id="145a2-127">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="145a2-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="145a2-128">q</span><span class="sxs-lookup"><span data-stu-id="145a2-128">q</span></span>              | <span data-ttu-id="145a2-129">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-129">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-130">Lunghezza primo, q, 20 byte.</span><span class="sxs-lookup"><span data-stu-id="145a2-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="145a2-131">Il bit più significativo del byte più significativo deve essere impostato su uno.</span><span class="sxs-lookup"><span data-stu-id="145a2-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="145a2-132">seedstruct</span><span class="sxs-lookup"><span data-stu-id="145a2-132">seedstruct</span></span>     | <span data-ttu-id="145a2-133">Struttura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="145a2-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="145a2-134">Valori di inizializzazione e contatore per la verifica dei numeri primi.</span><span class="sxs-lookup"><span data-stu-id="145a2-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="145a2-135">y</span><span class="sxs-lookup"><span data-stu-id="145a2-135">y</span></span>              | <span data-ttu-id="145a2-136">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-136">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-137">Chiave pubblica, y.</span><span class="sxs-lookup"><span data-stu-id="145a2-137">The public key, y.</span></span> <span data-ttu-id="145a2-138">Deve avere la stessa lunghezza di p.</span><span class="sxs-lookup"><span data-stu-id="145a2-138">Must be same length as p.</span></span> <span data-ttu-id="145a2-139">Se non ha la stessa lunghezza di p, deve essere riempita con 0x00 byte.</span><span class="sxs-lookup"><span data-stu-id="145a2-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="145a2-140">I [*BLOB di chiavi pubbliche*](../secgloss/p-gly.md) non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="145a2-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="145a2-141">Contengono chiavi pubbliche in formato [*testo non crittografato*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="145a2-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="145a2-142">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="145a2-142">Private Key BLOBs</span></span>

<span data-ttu-id="145a2-143">Una [*chiave privata*](../secgloss/p-gly.md) DSS viene esportata e importata come sequenza di byte strutturata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="145a2-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="145a2-144">Nella tabella seguente viene descritto ogni componente.</span><span class="sxs-lookup"><span data-stu-id="145a2-144">The following table describes each component.</span></span> <span data-ttu-id="145a2-145">Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="145a2-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="145a2-146">Campo</span><span class="sxs-lookup"><span data-stu-id="145a2-146">Field</span></span>          | <span data-ttu-id="145a2-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="145a2-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="145a2-148">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="145a2-148">dsspubkey</span></span>      | <span data-ttu-id="145a2-149">Struttura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="145a2-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="145a2-150">Il membro **Magic** deve essere impostato su 0x32535344.</span><span class="sxs-lookup"><span data-stu-id="145a2-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="145a2-151">Questo numero esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DSS2.</span><span class="sxs-lookup"><span data-stu-id="145a2-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="145a2-152">g</span><span class="sxs-lookup"><span data-stu-id="145a2-152">g</span></span>              | <span data-ttu-id="145a2-153">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-153">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-154">Il generatore, g.</span><span class="sxs-lookup"><span data-stu-id="145a2-154">The generator, g.</span></span> <span data-ttu-id="145a2-155">Deve avere la stessa lunghezza di p.</span><span class="sxs-lookup"><span data-stu-id="145a2-155">Must be the same length as p.</span></span> <span data-ttu-id="145a2-156">Se non ha la stessa lunghezza di p, deve essere riempita con 0x00 byte.</span><span class="sxs-lookup"><span data-stu-id="145a2-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="145a2-157">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="145a2-157">publickeystruc</span></span> | <span data-ttu-id="145a2-158">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="145a2-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="145a2-159">p</span><span class="sxs-lookup"><span data-stu-id="145a2-159">p</span></span>              | <span data-ttu-id="145a2-160">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-160">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-161">Il modulo principale, p.</span><span class="sxs-lookup"><span data-stu-id="145a2-161">The prime modulus, p.</span></span> <span data-ttu-id="145a2-162">Il bit più significativo del byte più significativo deve essere impostato su uno.</span><span class="sxs-lookup"><span data-stu-id="145a2-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="145a2-163">q</span><span class="sxs-lookup"><span data-stu-id="145a2-163">q</span></span>              | <span data-ttu-id="145a2-164">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-164">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-165">Il primo, q.</span><span class="sxs-lookup"><span data-stu-id="145a2-165">The prime, q.</span></span> <span data-ttu-id="145a2-166">q ha una lunghezza di 20 byte.</span><span class="sxs-lookup"><span data-stu-id="145a2-166">q is 20 bytes in length.</span></span> <span data-ttu-id="145a2-167">Il bit più significativo del byte più significativo deve essere impostato su uno.</span><span class="sxs-lookup"><span data-stu-id="145a2-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="145a2-168">seedstruct</span><span class="sxs-lookup"><span data-stu-id="145a2-168">seedstruct</span></span>     | <span data-ttu-id="145a2-169">Struttura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="145a2-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="145a2-170">Valori di inizializzazione e contatore per la verifica dei numeri primi.</span><span class="sxs-lookup"><span data-stu-id="145a2-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="145a2-171">x</span><span class="sxs-lookup"><span data-stu-id="145a2-171">x</span></span>              | <span data-ttu-id="145a2-172">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="145a2-172">A **BYTE** sequence.</span></span> <span data-ttu-id="145a2-173">Esponente del segreto, x.</span><span class="sxs-lookup"><span data-stu-id="145a2-173">The secret exponent, x.</span></span> <span data-ttu-id="145a2-174">Deve avere sempre una lunghezza di 20 byte.</span><span class="sxs-lookup"><span data-stu-id="145a2-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="145a2-175">Se x è di lunghezza inferiore a 20 byte, deve essere riempito con 0x00.</span><span class="sxs-lookup"><span data-stu-id="145a2-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="145a2-176">Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave.</span><span class="sxs-lookup"><span data-stu-id="145a2-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="145a2-177">**PRIVATEKEYBLOB** viene crittografato se il parametro *hExpKey* contiene un handle valido per una chiave di sessione.</span><span class="sxs-lookup"><span data-stu-id="145a2-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="145a2-178">Tutto tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata.</span><span class="sxs-lookup"><span data-stu-id="145a2-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="145a2-179">L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="145a2-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="145a2-180">L'applicazione deve gestire e archiviare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="145a2-180">The application must manage and store this information.</span></span> <span data-ttu-id="145a2-181">Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.</span><span class="sxs-lookup"><span data-stu-id="145a2-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="145a2-182">È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.</span><span class="sxs-lookup"><span data-stu-id="145a2-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
