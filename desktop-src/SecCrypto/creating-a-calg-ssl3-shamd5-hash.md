---
description: Viene illustrato come creare un \_ hash CALG SSL3 \_ SHAMD5.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Creazione di un hash di CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314134"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="0296d-103">Creazione di un \_ hash CALG SSL3 \_ SHAMD5</span><span class="sxs-lookup"><span data-stu-id="0296d-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="0296d-104">**Per creare un \_ hash CALG SSL3 \_ SHAMD5**</span><span class="sxs-lookup"><span data-stu-id="0296d-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="0296d-105">Usando la metodologia CryptoAPI standard, creare sia un MD5 che un [*hash*](../secgloss/h-gly.md) [*Sha*](../secgloss/s-gly.md) dei dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0296d-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="0296d-106">Concatena i due hash, con il valore MD5 più a sinistra e il valore SHA a destra.</span><span class="sxs-lookup"><span data-stu-id="0296d-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="0296d-107">Il risultato è un valore di 36 byte (16 byte + 20 byte).</span><span class="sxs-lookup"><span data-stu-id="0296d-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="0296d-108">Ottenere un handle per un [*oggetto hash*](../secgloss/h-gly.md) chiamando [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con CALG \_ SSL3 \_ SHAMD5 passato nel parametro *algido* .</span><span class="sxs-lookup"><span data-stu-id="0296d-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="0296d-109">Impostare il valore hash con una chiamata a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span><span class="sxs-lookup"><span data-stu-id="0296d-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="0296d-110">I valori hash concatenati vengono passati come **byte** \* nel parametro *PBDATA* e il \_ valore HP HASHVAL deve essere passato nel parametro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="0296d-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="0296d-111">La chiamata di [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con l'handle restituito da [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) nel passaggio 3 avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0296d-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="0296d-112">Chiamare [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) per generare la firma.</span><span class="sxs-lookup"><span data-stu-id="0296d-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="0296d-113">Chiamare [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) per eliminare definitivamente l'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="0296d-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 
