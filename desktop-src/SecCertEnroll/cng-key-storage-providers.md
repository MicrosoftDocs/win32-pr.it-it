---
description: "A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia da provider di archiviazione chiavi (KSP)."
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Provider di archiviazione chiavi CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401600"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="ebf92-103">Provider di archiviazione chiavi CNG</span><span class="sxs-lookup"><span data-stu-id="ebf92-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="ebf92-104">A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia da provider di archiviazione chiavi (KSP).</span><span class="sxs-lookup"><span data-stu-id="ebf92-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="ebf92-105">KSP può essere utilizzato per creare, eliminare, esportare, importare, aprire e archiviare chiavi.</span><span class="sxs-lookup"><span data-stu-id="ebf92-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="ebf92-106">A seconda dell'implementazione, possono essere usati anche per la crittografia asimmetrica, il segreto e la firma.</span><span class="sxs-lookup"><span data-stu-id="ebf92-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="ebf92-107">Microsoft installa i KSP seguenti a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ebf92-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ebf92-108">I fornitori possono creare e installare altri provider.</span><span class="sxs-lookup"><span data-stu-id="ebf92-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="ebf92-109">Provider di archiviazione chiavi del software Microsoft</span><span class="sxs-lookup"><span data-stu-id="ebf92-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="ebf92-110">Supporta la creazione e l'archiviazione delle chiavi software e gli algoritmi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebf92-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="ebf92-111">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="ebf92-111">Algorithm</span></span>                                          | <span data-ttu-id="ebf92-112">Scopo</span><span class="sxs-lookup"><span data-stu-id="ebf92-112">Purpose</span></span>                           | <span data-ttu-id="ebf92-113">Lunghezza chiave (BITS)</span><span class="sxs-lookup"><span data-stu-id="ebf92-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="ebf92-114">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="ebf92-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="ebf92-115">Contratto segreto e scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="ebf92-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebf92-116">da 512 a 4096 in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="ebf92-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="ebf92-117">Algoritmo di firma digitale (DSA)</span><span class="sxs-lookup"><span data-stu-id="ebf92-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="ebf92-118">Firme</span><span class="sxs-lookup"><span data-stu-id="ebf92-118">Signatures</span></span>                        | <span data-ttu-id="ebf92-119">da 512 a 1024 in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="ebf92-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="ebf92-120">Diffie-Hellman a curva ellittica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="ebf92-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="ebf92-121">Contratto segreto e scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="ebf92-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebf92-122">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebf92-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebf92-123">Algoritmo di firma digitale a curva ellittica (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="ebf92-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="ebf92-124">Firme</span><span class="sxs-lookup"><span data-stu-id="ebf92-124">Signatures</span></span>                        | <span data-ttu-id="ebf92-125">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebf92-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebf92-126">RSA</span><span class="sxs-lookup"><span data-stu-id="ebf92-126">RSA</span></span>                                                | <span data-ttu-id="ebf92-127">Crittografia e firma asimmetrica</span><span class="sxs-lookup"><span data-stu-id="ebf92-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="ebf92-128">da 512 a 16384 in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="ebf92-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="ebf92-129">Provider di archiviazione chiavi per Smart Card Microsoft</span><span class="sxs-lookup"><span data-stu-id="ebf92-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="ebf92-130">Supporta la creazione e l'archiviazione delle chiavi smart card e gli algoritmi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebf92-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="ebf92-131">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="ebf92-131">Algorithm</span></span>                                          | <span data-ttu-id="ebf92-132">Scopo</span><span class="sxs-lookup"><span data-stu-id="ebf92-132">Purpose</span></span>                           | <span data-ttu-id="ebf92-133">Lunghezza chiave (BITS)</span><span class="sxs-lookup"><span data-stu-id="ebf92-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="ebf92-134">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="ebf92-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="ebf92-135">Contratto segreto e scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="ebf92-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebf92-136">da 512 a 4096 in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="ebf92-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="ebf92-137">Diffie-Hellman a curva ellittica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="ebf92-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="ebf92-138">Contratto segreto e scambio di chiave</span><span class="sxs-lookup"><span data-stu-id="ebf92-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebf92-139">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebf92-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebf92-140">Algoritmo di firma digitale a curva ellittica (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="ebf92-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="ebf92-141">Firme</span><span class="sxs-lookup"><span data-stu-id="ebf92-141">Signatures</span></span>                        | <span data-ttu-id="ebf92-142">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebf92-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebf92-143">RSA</span><span class="sxs-lookup"><span data-stu-id="ebf92-143">RSA</span></span>                                                | <span data-ttu-id="ebf92-144">Crittografia e firma asimmetrica</span><span class="sxs-lookup"><span data-stu-id="ebf92-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="ebf92-145">da 512 a 16384 in incrementi di 64 bit</span><span class="sxs-lookup"><span data-stu-id="ebf92-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ebf92-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebf92-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf92-147">**Identificatori dell'algoritmo CNG**</span><span class="sxs-lookup"><span data-stu-id="ebf92-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="ebf92-148">Funzioni di archiviazione chiavi CNG</span><span class="sxs-lookup"><span data-stu-id="ebf92-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="ebf92-149">Informazioni sui provider di crittografia</span><span class="sxs-lookup"><span data-stu-id="ebf92-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
