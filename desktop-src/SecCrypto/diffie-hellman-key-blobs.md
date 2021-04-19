---
description: I BLOB vengono utilizzati con il provider di Diffie-Hellman per esportare chiavi da e importare chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: BLOB di chiavi di Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311929"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="891a6-103">BLOB di chiavi di Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="891a6-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="891a6-104">I [*BLOB*](../secgloss/b-gly.md) vengono usati con il provider [*Diffie-Hellman*](../secgloss/d-gly.md) per esportare le chiavi da e importare le chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="891a6-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="891a6-105">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="891a6-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="891a6-106">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="891a6-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="891a6-107">BLOB di chiavi pubbliche</span><span class="sxs-lookup"><span data-stu-id="891a6-107">Public Key BLOBs</span></span>

<span data-ttu-id="891a6-108">Diffie-Hellman [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per scambiare il valore (G ^ X) mod P in uno scambio di chiave Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="891a6-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="891a6-109">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="891a6-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="891a6-110">La tabella seguente descrive ogni componente del [*BLOB della chiave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="891a6-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="891a6-111">Campo</span><span class="sxs-lookup"><span data-stu-id="891a6-111">Field</span></span>          | <span data-ttu-id="891a6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="891a6-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891a6-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="891a6-113">dhpubkey</span></span>       | <span data-ttu-id="891a6-114">Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="891a6-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="891a6-115">Il membro **Magic** deve essere impostato su 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="891a6-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="891a6-116">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) "DH1".</span><span class="sxs-lookup"><span data-stu-id="891a6-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="891a6-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="891a6-117">publickeystruc</span></span> | <span data-ttu-id="891a6-118">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="891a6-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="891a6-119">y</span><span class="sxs-lookup"><span data-stu-id="891a6-119">y</span></span>              | <span data-ttu-id="891a6-120">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="891a6-120">A **BYTE** sequence.</span></span> <span data-ttu-id="891a6-121">Il valore Y, (G ^ X) mod P, si trova immediatamente dopo la struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) e deve essere sempre la lunghezza, in byte, del campo **bitlen DHPUBKEY** (lunghezza in bit di P) divisa per otto.</span><span class="sxs-lookup"><span data-stu-id="891a6-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="891a6-122">Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="891a6-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="891a6-123">BLOB di chiavi private</span><span class="sxs-lookup"><span data-stu-id="891a6-123">Private Key BLOBs</span></span>

<span data-ttu-id="891a6-124">Diffie-Hellman [*BLOB di chiavi private*](../secgloss/p-gly.md), digitare **PRIVATEKEYBLOB**, per archiviare le informazioni pubbliche/private di una chiave di Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="891a6-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="891a6-125">Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="891a6-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="891a6-126">La tabella seguente descrive ogni componente del BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="891a6-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="891a6-127">Campo</span><span class="sxs-lookup"><span data-stu-id="891a6-127">Field</span></span>          | <span data-ttu-id="891a6-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="891a6-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891a6-129">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="891a6-129">dhpubkey</span></span>       | <span data-ttu-id="891a6-130">Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="891a6-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="891a6-131">Il membro **Magic** deve essere impostato su 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="891a6-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="891a6-132">Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) "DH2".</span><span class="sxs-lookup"><span data-stu-id="891a6-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="891a6-133">generatore</span><span class="sxs-lookup"><span data-stu-id="891a6-133">generator</span></span>      | <span data-ttu-id="891a6-134">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="891a6-134">A **BYTE** sequence.</span></span> <span data-ttu-id="891a6-135">Il generatore, G.</span><span class="sxs-lookup"><span data-stu-id="891a6-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="891a6-136">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="891a6-136">publickeystruc</span></span> | <span data-ttu-id="891a6-137">Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="891a6-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="891a6-138">primo</span><span class="sxs-lookup"><span data-stu-id="891a6-138">prime</span></span>          | <span data-ttu-id="891a6-139">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="891a6-139">A **BYTE** sequence.</span></span> <span data-ttu-id="891a6-140">Il modulo principale, P. Questi dati devono sempre avere il bit più significativo del set di byte più significativo su uno.</span><span class="sxs-lookup"><span data-stu-id="891a6-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="891a6-141">secret</span><span class="sxs-lookup"><span data-stu-id="891a6-141">secret</span></span>         | <span data-ttu-id="891a6-142">Sequenza di **byte** .</span><span class="sxs-lookup"><span data-stu-id="891a6-142">A **BYTE** sequence.</span></span> <span data-ttu-id="891a6-143">Esponente del segreto, X.</span><span class="sxs-lookup"><span data-stu-id="891a6-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="891a6-144">Il generatore e il segreto devono avere sempre la stessa lunghezza, in byte.</span><span class="sxs-lookup"><span data-stu-id="891a6-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="891a6-145">Se il valore di è uno o più più breve dell'altro, deve essere riempito con il numero necessario di byte di valore pari a zero per renderli uguali.</span><span class="sxs-lookup"><span data-stu-id="891a6-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="891a6-146">Il generatore e il segreto sono in formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="891a6-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
