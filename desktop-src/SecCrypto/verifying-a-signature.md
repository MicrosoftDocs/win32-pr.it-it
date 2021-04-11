---
description: Per verificare una firma, creare un oggetto hash usando CryptCreateHash. Questo oggetto hash accumula i dati da verificare. I dati vengono quindi aggiunti all'oggetto hash con la funzione CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Verifica di una firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130226"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="b5b11-105">Verifica di una firma</span><span class="sxs-lookup"><span data-stu-id="b5b11-105">Verifying a Signature</span></span>

<span data-ttu-id="b5b11-106">Per verificare una firma, creare un [*oggetto hash*](../secgloss/h-gly.md) usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="b5b11-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="b5b11-107">Questo oggetto hash accumula i dati da verificare.</span><span class="sxs-lookup"><span data-stu-id="b5b11-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="b5b11-108">I dati vengono quindi aggiunti all'oggetto hash con la funzione [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="b5b11-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="b5b11-109">Dopo l'aggiunta dell'ultimo blocco di dati all'hash, utilizzare [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) per verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="b5b11-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="b5b11-110">L'indirizzo dei dati della firma, un handle per l'oggetto hash e l'handle delle chiavi pubbliche vengono passati a **CryptVerifySignature**.</span><span class="sxs-lookup"><span data-stu-id="b5b11-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="b5b11-111">Dopo che la firma è stata verificata (o non ha superato la verifica), eliminare definitivamente l'oggetto hash usando la funzione [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="b5b11-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 
