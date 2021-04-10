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
# <a name="initiating-a-copp-session"></a>Avvio di una sessione COPP

Per avviare una sessione COPP (Certified Output Protocol), è necessario preparare una *firma*, ovvero una matrice che contiene la concatenazione dei numeri seguenti:

-   Numero casuale a 128 bit restituito dal driver. Questo valore viene visualizzato come *guidRandom* per [ottenere la catena di certificati del driver](obtaining-the-drivers-certificate-chain.md).
-   Chiave AES simmetrica a 128 bit.
-   Numero di sequenza iniziale a 32 bit per le richieste di stato.
-   Numero di sequenza iniziale a 32 bit per i comandi COPP.

Generare una chiave AES simmetrica come segue:


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



La funzione **CryptGenKey** crea la chiave simmetrica, ma la chiave viene ancora mantenuta nel CSP. Per esportare la chiave in una matrice di byte, usare la funzione **CryptExportKey** . Questo è il motivo per cui viene utilizzato il \_ flag esportabile Crypt quando si chiama **CryptGenKey**. Il codice seguente esporta la chiave e la copia nel


```
pData
```



matrice.


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



Dati restituiti in


```
pData
```



dispone del layout seguente:


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



Tuttavia, nessuna struttura corrispondente a questo layout è definita nelle intestazioni CryptoAPI. È possibile definire una o più operazioni aritmetiche del puntatore. Ad esempio, per verificare le dimensioni della chiave:


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



Per ottenere il puntatore alla chiave stessa:


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



Generare quindi un numero casuale a 32 bit da usare come sequenza iniziale per le richieste di stato di COPP. Il metodo consigliato per creare un numero casuale consiste nel chiamare la funzione **CryptGenRandom** . Non usare la funzione **Rand** nella libreria di runtime del linguaggio C perché non è realmente casuale. Generare un secondo numero casuale a 32 bit da usare come sequenza iniziale per i comandi COPP.


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



A questo punto è possibile preparare la firma COPP. Si tratta di una matrice di 256 byte, definita come struttura [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) . Inizializzare il contenuto della matrice su zero. Copiare quindi i quattro numeri nell'array, ovvero il numero casuale del driver, la chiave AES, il numero di sequenza dello stato e il numero di sequenza del comando, in questo ordine. Infine, scambiare l'ordine dei byte dell'intera matrice.

In base alla documentazione per **CryptEncrypt**:

<dl> "La lunghezza dei dati in testo non crittografato che possono essere crittografati con una chiamata a **CryptEncrypt** con una chiave RSA è la lunghezza del modulo della chiave meno undici byte. Gli undici byte corrispondono al minimo scelto per il \# riempimento PKCS 1 ".  
</dl>

In questo caso, il modulo è 256 byte, quindi la lunghezza massima dei messaggi è 245 byte (256 – 11). La struttura **AMCOPPSignature** è 256 byte, ma i dati significativi nella firma sono solo 40 byte. Il codice seguente crittografa la firma e fornisce il risultato in


```
CoppSig
```



.


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



Passare ora la matrice crittografata a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



Se questo metodo ha esito positivo, si è pronti per inviare i comandi di COPP e le richieste di stato al driver.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



