---
description: I BLOB vengono utilizzati con il provider Diffie-Hellman/SChannel per esportare le chiavi da e importare le chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: BLOB di chiavi Diffie-Hellman/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756536"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="d5d90-103">BLOB di chiavi Diffie-Hellman/SChannel</span><span class="sxs-lookup"><span data-stu-id="d5d90-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="d5d90-104">I [*BLOB*](../secgloss/b-gly.md) vengono utilizzati con il provider Schannel [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) per esportare chiavi da e importare chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="d5d90-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="d5d90-105">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="d5d90-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="d5d90-106">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="d5d90-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="d5d90-107">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="d5d90-107">Public Key BLOBs</span></span>

<span data-ttu-id="d5d90-108">Diffie-Hellman [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per scambiare il valore (G ^ X) mod P in uno scambio di chiave Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="d5d90-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="d5d90-109">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="d5d90-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="d5d90-110">La tabella seguente descrive ogni componente del [*BLOB della chiave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d5d90-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="d5d90-111">Campo</span><span class="sxs-lookup"><span data-stu-id="d5d90-111">Field</span></span>          | <span data-ttu-id="d5d90-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d90-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d90-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="d5d90-113">dhpubkey</span></span>       | <span data-ttu-id="d5d90-114">Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="d5d90-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="d5d90-115">Il membro **Magic** deve essere impostato su 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="d5d90-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="d5d90-116">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DH1.</span><span class="sxs-lookup"><span data-stu-id="d5d90-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d5d90-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="d5d90-117">publickeystruc</span></span> | <span data-ttu-id="d5d90-118">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="d5d90-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d5d90-119">y</span><span class="sxs-lookup"><span data-stu-id="d5d90-119">y</span></span>              | <span data-ttu-id="d5d90-120">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="d5d90-120">A **BYTE** sequence.</span></span> <span data-ttu-id="d5d90-121">Il valore y, (G ^ X) mod P, si trova immediatamente dopo la struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="d5d90-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="d5d90-122">La lunghezza, in byte, della sequenza è il membro **bitlen** di **DHPUBKEY** diviso 8.</span><span class="sxs-lookup"><span data-stu-id="d5d90-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="d5d90-123">Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="d5d90-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="d5d90-124">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="d5d90-124">Private Key BLOBs</span></span>

<span data-ttu-id="d5d90-125">I BLOB di [*chiavi private*](../secgloss/p-gly.md)d-h, digitare **PRIVATEKEYBLOB**, vengono usati per esportare e importare informazioni private di una chiave D-h.</span><span class="sxs-lookup"><span data-stu-id="d5d90-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="d5d90-126">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="d5d90-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="d5d90-127">La tabella seguente descrive ogni componente del BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="d5d90-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="d5d90-128">Campo</span><span class="sxs-lookup"><span data-stu-id="d5d90-128">Field</span></span>          | <span data-ttu-id="d5d90-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d90-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d90-130">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="d5d90-130">dhpubkey</span></span>       | <span data-ttu-id="d5d90-131">Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="d5d90-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="d5d90-132">Il membro **Magic** deve essere impostato su 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="d5d90-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="d5d90-133">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DH2.</span><span class="sxs-lookup"><span data-stu-id="d5d90-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="d5d90-134">generatore</span><span class="sxs-lookup"><span data-stu-id="d5d90-134">generator</span></span>      | <span data-ttu-id="d5d90-135">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="d5d90-135">A **BYTE** sequence.</span></span> <span data-ttu-id="d5d90-136">Il generatore G.</span><span class="sxs-lookup"><span data-stu-id="d5d90-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="d5d90-137">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="d5d90-137">publickeystruc</span></span> | <span data-ttu-id="d5d90-138">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="d5d90-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="d5d90-139">primo</span><span class="sxs-lookup"><span data-stu-id="d5d90-139">prime</span></span>          | <span data-ttu-id="d5d90-140">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="d5d90-140">A **BYTE** sequence.</span></span> <span data-ttu-id="d5d90-141">Il modulo principale, P. Questi dati devono sempre avere il bit più significativo del set di byte più significativo su uno.</span><span class="sxs-lookup"><span data-stu-id="d5d90-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="d5d90-142">secret</span><span class="sxs-lookup"><span data-stu-id="d5d90-142">secret</span></span>         | <span data-ttu-id="d5d90-143">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="d5d90-143">A **BYTE** sequence.</span></span> <span data-ttu-id="d5d90-144">Esponente del segreto X.</span><span class="sxs-lookup"><span data-stu-id="d5d90-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="d5d90-145">I valori primo, generatore e segreto devono sempre avere la stessa lunghezza, in byte.</span><span class="sxs-lookup"><span data-stu-id="d5d90-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="d5d90-146">Se un valore è un byte o più più breve di quello degli altri, deve essere riempito con il numero necessario di zero byte per renderli uguali.</span><span class="sxs-lookup"><span data-stu-id="d5d90-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="d5d90-147">Il primo, il generatore e il segreto sono in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d5d90-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
