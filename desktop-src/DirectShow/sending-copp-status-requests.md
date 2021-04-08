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
# <a name="sending-copp-status-requests"></a><span data-ttu-id="80fe4-103">Invio di richieste di stato di COPP</span><span class="sxs-lookup"><span data-stu-id="80fe4-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="80fe4-104">Per inviare una richiesta di stato COPP (Certified Output Protocol), compilare una struttura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) con i dati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="80fe4-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="80fe4-105">I membri della struttura sono:</span><span class="sxs-lookup"><span data-stu-id="80fe4-105">The structure members are:</span></span>

-   <span data-ttu-id="80fe4-106">**rApp**.</span><span class="sxs-lookup"><span data-stu-id="80fe4-106">**rApp**.</span></span> <span data-ttu-id="80fe4-107">Numero casuale a 128 bit, tipizzato come GUID.</span><span class="sxs-lookup"><span data-stu-id="80fe4-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="80fe4-108">Lo stesso numero viene restituito nella risposta del driver.</span><span class="sxs-lookup"><span data-stu-id="80fe4-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="80fe4-109">È necessario allocare il numero casuale nell'heap e quindi copiarlo nella struttura.</span><span class="sxs-lookup"><span data-stu-id="80fe4-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="80fe4-110">Questo protegge dagli attacchi in cui l'autore dell'attacco modifica il contenuto della struttura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) .</span><span class="sxs-lookup"><span data-stu-id="80fe4-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="80fe4-111">**guidStatusRequestID**.</span><span class="sxs-lookup"><span data-stu-id="80fe4-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="80fe4-112">GUID che identifica la richiesta.</span><span class="sxs-lookup"><span data-stu-id="80fe4-112">A GUID that identifies the request.</span></span> <span data-ttu-id="80fe4-113">Vedere [Copp query Reference](copp-query-reference.md).</span><span class="sxs-lookup"><span data-stu-id="80fe4-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="80fe4-114">**dwSequence**.</span><span class="sxs-lookup"><span data-stu-id="80fe4-114">**dwSequence**.</span></span> <span data-ttu-id="80fe4-115">Numero di sequenza dello stato.</span><span class="sxs-lookup"><span data-stu-id="80fe4-115">The status sequence number.</span></span> <span data-ttu-id="80fe4-116">Incrementare questo valore dopo ogni richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="80fe4-116">Increment this value after each status request.</span></span> <span data-ttu-id="80fe4-117">Nella sezione relativa all' [avvio di una sessione COPP](initiating-a-copp-session.md), questo valore viene mostrato come *uStatusSeq* negli esempi di codice.</span><span class="sxs-lookup"><span data-stu-id="80fe4-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="80fe4-118">**cbSizeData**.</span><span class="sxs-lookup"><span data-stu-id="80fe4-118">**cbSizeData**.</span></span> <span data-ttu-id="80fe4-119">Dimensioni, in byte, dei dati aggiuntivi necessari per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="80fe4-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="80fe4-120">**StatusData**.</span><span class="sxs-lookup"><span data-stu-id="80fe4-120">**StatusData**.</span></span> <span data-ttu-id="80fe4-121">Dati per la richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="80fe4-121">Data for the status request.</span></span>

<span data-ttu-id="80fe4-122">Passare la struttura [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) al metodo [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) .</span><span class="sxs-lookup"><span data-stu-id="80fe4-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="80fe4-123">Ad esempio, il codice seguente invia una richiesta di stato che esegue query sui meccanismi di protezione disponibili:</span><span class="sxs-lookup"><span data-stu-id="80fe4-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


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



<span data-ttu-id="80fe4-124">La risposta viene scritta nel membro **COPPStatus** della struttura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) .</span><span class="sxs-lookup"><span data-stu-id="80fe4-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="80fe4-125">Le dimensioni dei dati validi nella risposta sono fornite nel membro **cbSizeData** .</span><span class="sxs-lookup"><span data-stu-id="80fe4-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="80fe4-126">Per garantire l'integrità del messaggio, il driver calcola un codice MAC (Message Authentication Code) usando l'algoritmo OMAC 1 e restituisce questo valore nel membro **macKDI** della struttura.</span><span class="sxs-lookup"><span data-stu-id="80fe4-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="80fe4-127">L'applicazione deve verificare questo valore come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="80fe4-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="80fe4-128">Calcolare il tag OMAC per il blocco di dati visualizzato dopo il membro **macKDI** della struttura [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (in altre parole, **cbSizeData** più **COPPStatus**).</span><span class="sxs-lookup"><span data-stu-id="80fe4-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="80fe4-129">Confrontare questo tag con il valore in **macKDI**, usando un **memcmp** dritto.</span><span class="sxs-lookup"><span data-stu-id="80fe4-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="80fe4-130">L'algoritmo OMAC 1 è descritto in dettaglio in [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) .</span><span class="sxs-lookup"><span data-stu-id="80fe4-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="80fe4-131">COPP usa i seguenti parametri OMAC-1:</span><span class="sxs-lookup"><span data-stu-id="80fe4-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="80fe4-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="80fe4-132">E = AES</span></span>
-   <span data-ttu-id="80fe4-133">t = 128 bit</span><span class="sxs-lookup"><span data-stu-id="80fe4-133">t = 128 bits</span></span>

<span data-ttu-id="80fe4-134">I dati restituiti dalla richiesta di stato iniziano sempre con due elementi:</span><span class="sxs-lookup"><span data-stu-id="80fe4-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="80fe4-135">Lo stesso valore di **rApp** passato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80fe4-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="80fe4-136">È necessario verificare che questo valore corrisponda al valore originale archiviato nell'heap.</span><span class="sxs-lookup"><span data-stu-id="80fe4-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="80fe4-137">Valore [**di \_ StatusFlags Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) che indica se lo stato di protezione dell'output è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="80fe4-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="80fe4-138">Poiché la connessione può essere persa o riconfigurata, l'applicazione deve eseguire periodicamente il polling del driver per lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="80fe4-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="80fe4-139">Se \_ viene impostato il flag Copp RenegotiationRequired, l'applicazione deve tentare di reimpostare il livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="80fe4-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="80fe4-140">Se \_ è impostato il flag Copp LinkLost, l'applicazione deve interrompere la riproduzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="80fe4-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="80fe4-141">Ad esempio, il \_ flag Copp LinkLost può essere restituito perché l'utente ha scollegato il connettore di output.</span><span class="sxs-lookup"><span data-stu-id="80fe4-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="80fe4-142">L'applicazione deve rilasciare l'istanza corrente di VMR, creare una nuova istanza di VMR e stabilire una nuova sessione COPP (incluso lo scambio di chiave e la convalida dei certificati).</span><span class="sxs-lookup"><span data-stu-id="80fe4-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80fe4-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80fe4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80fe4-144">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="80fe4-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



