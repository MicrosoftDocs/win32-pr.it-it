---
description: La crittografia è il processo di conversione di dati di testo normale (testo normale) in un elemento apparentemente casuale e non significativo (testo crittografato). La decrittografia è il processo di conversione del testo crittografato di nuovo in testo normale.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Crittografia e decrittografia dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128791"
---
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="4441a-104">Crittografia e decrittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="4441a-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="4441a-105">La crittografia è il processo di conversione di dati di testo normale [*(testo normale) in*](../secgloss/p-gly.md)un elemento apparentemente casuale e non significativo (testo [*crittografato*](../secgloss/c-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="4441a-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="4441a-106">La decrittografia è il processo di conversione del testo crittografato di nuovo in testo normale.</span><span class="sxs-lookup"><span data-stu-id="4441a-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="4441a-107">Per crittografare più di una piccola quantità di dati, viene utilizzata la [*crittografia simmetrica*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4441a-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="4441a-108">Una [*chiave simmetrica*](../secgloss/s-gly.md) viene utilizzata durante i processi di crittografia e decrittografia.</span><span class="sxs-lookup"><span data-stu-id="4441a-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="4441a-109">Per decrittografare una particolare parte del testo crittografato, è necessario usare la chiave usata per crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="4441a-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="4441a-110">L'obiettivo di ogni algoritmo di crittografia è renderlo il più difficile possibile per decrittografare il testo crittografato generato senza usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="4441a-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="4441a-111">Se viene usato un algoritmo di crittografia realmente valido, non sono disponibili tecniche significativamente migliori rispetto alla possibilità di provare ogni chiave possibile.</span><span class="sxs-lookup"><span data-stu-id="4441a-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="4441a-112">Per un algoritmo di questo tipo, più è lunga la chiave, più è difficile decrittografare un pezzo di testo crittografato senza avere la chiave.</span><span class="sxs-lookup"><span data-stu-id="4441a-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="4441a-113">È difficile determinare la qualità di un algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4441a-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="4441a-114">Gli algoritmi che sembrano promesse a volte diventano molto facili da interrompere, dato l'attacco appropriato.</span><span class="sxs-lookup"><span data-stu-id="4441a-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="4441a-115">Quando si seleziona un algoritmo di crittografia, è consigliabile sceglierne uno che è stato usato per diversi anni e che abbia superato tutti gli attacchi.</span><span class="sxs-lookup"><span data-stu-id="4441a-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="4441a-116">Per altre informazioni, vedere [funzioni di crittografia e decrittografia dei dati](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4441a-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
