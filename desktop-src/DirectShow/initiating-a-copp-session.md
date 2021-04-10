---
description: Avvio di una sessione COPP
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Avvio di una sessione COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125085"
---
# <a name="initiating-a-copp-session"></a><span data-ttu-id="bc45b-103">Avvio di una sessione COPP</span><span class="sxs-lookup"><span data-stu-id="bc45b-103">Initiating a COPP Session</span></span>

<span data-ttu-id="bc45b-104">Per avviare una sessione COPP (Certified Output Protocol), è necessario preparare una *firma*, ovvero una matrice che contiene la concatenazione dei numeri seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc45b-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="bc45b-105">Numero casuale a 128 bit restituito dal driver.</span><span class="sxs-lookup"><span data-stu-id="bc45b-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="bc45b-106">Questo valore viene visualizzato come *guidRandom* per [ottenere la catena di certificati del driver](obtaining-the-drivers-certificate-chain.md).</span><span class="sxs-lookup"><span data-stu-id="bc45b-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="bc45b-107">Chiave AES simmetrica a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="bc45b-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="bc45b-108">Numero di sequenza iniziale a 32 bit per le richieste di stato.</span><span class="sxs-lookup"><span data-stu-id="bc45b-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="bc45b-109">Numero di sequenza iniziale a 32 bit per i comandi COPP.</span><span class="sxs-lookup"><span data-stu-id="bc45b-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="bc45b-110">Generare una chiave AES simmetrica come segue:</span><span class="sxs-lookup"><span data-stu-id="bc45b-110">Generate a symmetric AES key as follows:</span></span>


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



<span data-ttu-id="bc45b-111">La funzione **CryptGenKey** crea la chiave simmetrica, ma la chiave viene ancora mantenuta nel CSP.</span><span class="sxs-lookup"><span data-stu-id="bc45b-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="bc45b-112">Per esportare la chiave in una matrice di byte, usare la funzione **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="bc45b-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="bc45b-113">Questo è il motivo per cui viene utilizzato il \_ flag esportabile Crypt quando si chiama **CryptGenKey**.</span><span class="sxs-lookup"><span data-stu-id="bc45b-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="bc45b-114">Il codice seguente esporta la chiave e la copia nel</span><span class="sxs-lookup"><span data-stu-id="bc45b-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="bc45b-115">matrice.</span><span class="sxs-lookup"><span data-stu-id="bc45b-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="bc45b-116">Dati restituiti in</span><span class="sxs-lookup"><span data-stu-id="bc45b-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="bc45b-117">dispone del layout seguente:</span><span class="sxs-lookup"><span data-stu-id="bc45b-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="bc45b-118">Tuttavia, nessuna struttura corrispondente a questo layout è definita nelle intestazioni CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="bc45b-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="bc45b-119">È possibile definire una o più operazioni aritmetiche del puntatore.</span><span class="sxs-lookup"><span data-stu-id="bc45b-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="bc45b-120">Ad esempio, per verificare le dimensioni della chiave:</span><span class="sxs-lookup"><span data-stu-id="bc45b-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="bc45b-121">Per ottenere il puntatore alla chiave stessa:</span><span class="sxs-lookup"><span data-stu-id="bc45b-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="bc45b-122">Generare quindi un numero casuale a 32 bit da usare come sequenza iniziale per le richieste di stato di COPP.</span><span class="sxs-lookup"><span data-stu-id="bc45b-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="bc45b-123">Il metodo consigliato per creare un numero casuale consiste nel chiamare la funzione **CryptGenRandom** .</span><span class="sxs-lookup"><span data-stu-id="bc45b-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="bc45b-124">Non usare la funzione **Rand** nella libreria di runtime del linguaggio C perché non è realmente casuale.</span><span class="sxs-lookup"><span data-stu-id="bc45b-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="bc45b-125">Generare un secondo numero casuale a 32 bit da usare come sequenza iniziale per i comandi COPP.</span><span class="sxs-lookup"><span data-stu-id="bc45b-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="bc45b-126">A questo punto è possibile preparare la firma COPP.</span><span class="sxs-lookup"><span data-stu-id="bc45b-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="bc45b-127">Si tratta di una matrice di 256 byte, definita come struttura [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) .</span><span class="sxs-lookup"><span data-stu-id="bc45b-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="bc45b-128">Inizializzare il contenuto della matrice su zero.</span><span class="sxs-lookup"><span data-stu-id="bc45b-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="bc45b-129">Copiare quindi i quattro numeri nell'array, ovvero il numero casuale del driver, la chiave AES, il numero di sequenza dello stato e il numero di sequenza del comando, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="bc45b-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="bc45b-130">Infine, scambiare l'ordine dei byte dell'intera matrice.</span><span class="sxs-lookup"><span data-stu-id="bc45b-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="bc45b-131">In base alla documentazione per **CryptEncrypt**:</span><span class="sxs-lookup"><span data-stu-id="bc45b-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="bc45b-132">"La lunghezza dei dati in testo non crittografato che possono essere crittografati con una chiamata a **CryptEncrypt** con una chiave RSA è la lunghezza del modulo della chiave meno undici byte.</span><span class="sxs-lookup"><span data-stu-id="bc45b-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="bc45b-133">Gli undici byte corrispondono al minimo scelto per il \# riempimento PKCS 1 ".</span><span class="sxs-lookup"><span data-stu-id="bc45b-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="bc45b-134">In questo caso, il modulo è 256 byte, quindi la lunghezza massima dei messaggi è 245 byte (256 – 11).</span><span class="sxs-lookup"><span data-stu-id="bc45b-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="bc45b-135">La struttura **AMCOPPSignature** è 256 byte, ma i dati significativi nella firma sono solo 40 byte.</span><span class="sxs-lookup"><span data-stu-id="bc45b-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="bc45b-136">Il codice seguente crittografa la firma e fornisce il risultato in</span><span class="sxs-lookup"><span data-stu-id="bc45b-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="bc45b-137">.</span><span class="sxs-lookup"><span data-stu-id="bc45b-137">.</span></span>


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



<span data-ttu-id="bc45b-138">Passare ora la matrice crittografata a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span><span class="sxs-lookup"><span data-stu-id="bc45b-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="bc45b-139">Se questo metodo ha esito positivo, si è pronti per inviare i comandi di COPP e le richieste di stato al driver.</span><span class="sxs-lookup"><span data-stu-id="bc45b-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc45b-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc45b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc45b-141">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="bc45b-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



