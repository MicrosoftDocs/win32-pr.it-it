---
description: Un hash di un testo o di un'altra stringa di byte è un valore associato, statisticamente univoco a lunghezza fissa.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hash dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885070"
---
# <a name="data-hashes"></a><span data-ttu-id="d7e00-103">Hash dei dati</span><span class="sxs-lookup"><span data-stu-id="d7e00-103">Data Hashes</span></span>

<span data-ttu-id="d7e00-104">Un [*hash*](../secgloss/h-gly.md) di un testo o di un'altra stringa di byte è un valore associato, statisticamente univoco a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="d7e00-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="d7e00-105">In alcuni documenti, un *hash* di un testo viene anche definito digest; Tuttavia, in questa documentazione viene sempre usato il termine hash.</span><span class="sxs-lookup"><span data-stu-id="d7e00-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="d7e00-106">Le funzioni CryptoAPI forniscono un metodo per creare un hash per qualsiasi testo o altra stringa di byte.</span><span class="sxs-lookup"><span data-stu-id="d7e00-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="d7e00-107">Tale hash, quindi, può essere utilizzato come identificatore univoco dei dati associati.</span><span class="sxs-lookup"><span data-stu-id="d7e00-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="d7e00-108">Per garantire l' [*integrità*](../secgloss/i-gly.md) di un testo, è possibile inviare un [*hash*](../secgloss/h-gly.md) di un testo per accompagnare il testo.</span><span class="sxs-lookup"><span data-stu-id="d7e00-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="d7e00-109">Il ricevitore può quindi calcolare un hash sui dati ricevuti e confrontare l'hash calcolato con l'hash ricevuto.</span><span class="sxs-lookup"><span data-stu-id="d7e00-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="d7e00-110">Se le due corrispondenze, i dati ricevuti devono corrispondere ai dati da cui è stato creato l'hash ricevuto.</span><span class="sxs-lookup"><span data-stu-id="d7e00-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="d7e00-111">Per ottenere un valore hash, creare un oggetto hash usando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="d7e00-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="d7e00-112">Questo oggetto accumulerà i dati da verificare.</span><span class="sxs-lookup"><span data-stu-id="d7e00-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="d7e00-113">I dati vengono quindi aggiunti all'oggetto hash con la funzione [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="d7e00-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="d7e00-114">Dopo l'aggiunta dell'ultimo blocco di dati all'hash, viene usata la funzione [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) per ottenere il valore hash dei dati.</span><span class="sxs-lookup"><span data-stu-id="d7e00-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="d7e00-115">Viene garantita una migliore sicurezza eliminando l'oggetto hash con [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) non appena viene ottenuto il valore hash.</span><span class="sxs-lookup"><span data-stu-id="d7e00-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
