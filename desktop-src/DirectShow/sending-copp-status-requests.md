---
description: Invio di richieste di stato di COPP
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Invio di richieste di stato di COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745415"
---
# <a name="sending-copp-status-requests"></a>Invio di richieste di stato di COPP

Per inviare una richiesta di stato COPP (Certified Output Protocol), compilare una struttura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) con i dati della richiesta. I membri della struttura sono:

-   **rApp**. Numero casuale a 128 bit, tipizzato come GUID. Lo stesso numero viene restituito nella risposta del driver. È necessario allocare il numero casuale nell'heap e quindi copiarlo nella struttura. Questo protegge dagli attacchi in cui l'autore dell'attacco modifica il contenuto della struttura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .
-   **guidStatusRequestID**. GUID che identifica la richiesta. Vedere [Copp query Reference](copp-query-reference.md).
-   **dwSequence**. Numero di sequenza dello stato. Incrementare questo valore dopo ogni richiesta di stato. Nella sezione relativa all' [avvio di una sessione COPP](initiating-a-copp-session.md), questo valore viene mostrato come *uStatusSeq* negli esempi di codice.
-   **cbSizeData**. Dimensioni, in byte, dei dati aggiuntivi necessari per la richiesta.
-   **StatusData**. Dati per la richiesta di stato.

Passare la struttura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) al metodo [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) . Ad esempio, il codice seguente invia una richiesta di stato che esegue query sui meccanismi di protezione disponibili:


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



La risposta viene scritta nel membro **COPPStatus** della struttura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) . Le dimensioni dei dati validi nella risposta sono fornite nel membro **cbSizeData** . Per garantire l'integrità del messaggio, il driver calcola un codice MAC (Message Authentication Code) usando l'algoritmo OMAC 1 e restituisce questo valore nel membro **macKDI** della struttura. L'applicazione deve verificare questo valore come indicato di seguito:

1.  Calcolare il tag OMAC per il blocco di dati visualizzato dopo il membro **macKDI** della struttura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (in altre parole, **cbSizeData** più **COPPStatus**).
2.  Confrontare questo tag con il valore in **macKDI**, usando un **memcmp** dritto.

L'algoritmo OMAC 1 è descritto in dettaglio in [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) . COPP usa i seguenti parametri OMAC-1:

-   E = AES
-   t = 128 bit

I dati restituiti dalla richiesta di stato iniziano sempre con due elementi:

-   Lo stesso valore di **rApp** passato dall'applicazione. È necessario verificare che questo valore corrisponda al valore originale archiviato nell'heap.
-   Valore [**di \_ StatusFlags Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) che indica se lo stato di protezione dell'output è stato modificato.

Poiché la connessione può essere persa o riconfigurata, l'applicazione deve eseguire periodicamente il polling del driver per lo stato corrente. Se \_ viene impostato il flag Copp RenegotiationRequired, l'applicazione deve tentare di reimpostare il livello di protezione. Se \_ è impostato il flag Copp LinkLost, l'applicazione deve interrompere la riproduzione del contenuto. Ad esempio, il \_ flag Copp LinkLost può essere restituito perché l'utente ha scollegato il connettore di output. L'applicazione deve rilasciare l'istanza corrente di VMR, creare una nuova istanza di VMR e stabilire una nuova sessione COPP (incluso lo scambio di chiave e la convalida dei certificati).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



