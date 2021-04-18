---
description: Panoramica di COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Panoramica di COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303963"
---
# <a name="overview-of-copp"></a><span data-ttu-id="db96d-103">Panoramica di COPP</span><span class="sxs-lookup"><span data-stu-id="db96d-103">Overview of COPP</span></span>

<span data-ttu-id="db96d-104">Di seguito sono riportati i passaggi di base che un'applicazione deve eseguire per usare il protocollo COPP (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="db96d-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="db96d-105">**Ottenere la catena di certificati del driver**</span><span class="sxs-lookup"><span data-stu-id="db96d-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="db96d-106">Creare un grafico di riproduzione DirectShow che esegua il rendering dei video usando il renderer di mixaggio video (VMR-7 o VMR-9) o il filtro [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="db96d-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="db96d-107">Eseguire una query su VMR per l'interfaccia [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .</span><span class="sxs-lookup"><span data-stu-id="db96d-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="db96d-108">Chiamare [**IAMCertifiedOutputProtection:: backexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="db96d-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="db96d-109">Questo metodo restituisce un numero casuale a 128 bit dal driver, insieme a una catena di certificati che contiene la chiave pubblica RSA a 2048 bit del driver.</span><span class="sxs-lookup"><span data-stu-id="db96d-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="db96d-110">**Convalidare la catena di certificati**</span><span class="sxs-lookup"><span data-stu-id="db96d-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="db96d-111">Convalidare la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="db96d-111">Validate the certificate chain.</span></span> <span data-ttu-id="db96d-112">Se la catena di certificati non è valida, arrestare.</span><span class="sxs-lookup"><span data-stu-id="db96d-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="db96d-113">Controllare l'elenco di revoche di certificati (CRL).</span><span class="sxs-lookup"><span data-stu-id="db96d-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="db96d-114">Se uno dei certificati nella catena di certificati viene visualizzato nell'elenco di revoche, arrestare.</span><span class="sxs-lookup"><span data-stu-id="db96d-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="db96d-115">Ottenere la chiave pubblica RSA dalla catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="db96d-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="db96d-116">**Inizializzare la sessione COPP**</span><span class="sxs-lookup"><span data-stu-id="db96d-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="db96d-117">Generare una chiave di sessione AES a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="db96d-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="db96d-118">Questa chiave viene utilizzata per firmare i dati e verificare che i dati firmati non siano stati manomessi.</span><span class="sxs-lookup"><span data-stu-id="db96d-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="db96d-119">Genera due numeri casuali a 32 bit a crittografia sicura.</span><span class="sxs-lookup"><span data-stu-id="db96d-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="db96d-120">Il primo è un numero di sequenza di stato, il secondo è un numero di sequenza di comandi.</span><span class="sxs-lookup"><span data-stu-id="db96d-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="db96d-121">Ogni volta che l'applicazione invia una richiesta di comando o di stato, incrementa il numero di sequenza corrispondente e include questo numero nel comando COPP o nei dati della richiesta.</span><span class="sxs-lookup"><span data-stu-id="db96d-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="db96d-122">Concatenare il numero casuale a 128 bit dal driver della grafica, la chiave della sessione AES, il numero di sequenza dello stato e il numero di sequenza del comando.</span><span class="sxs-lookup"><span data-stu-id="db96d-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="db96d-123">Crittografare questa matrice di byte utilizzando la chiave pubblica del driver e passare il risultato a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span><span class="sxs-lookup"><span data-stu-id="db96d-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="db96d-124">**Inviare comandi di COPP e richieste di stato**</span><span class="sxs-lookup"><span data-stu-id="db96d-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="db96d-125">Eseguire una query per i tipi di protezione disponibili e altre informazioni chiamando [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span><span class="sxs-lookup"><span data-stu-id="db96d-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="db96d-126">Impostare i livelli di protezione desiderati chiamando [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span><span class="sxs-lookup"><span data-stu-id="db96d-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="db96d-127">Eseguire periodicamente una query per il livello di protezione locale corrente.</span><span class="sxs-lookup"><span data-stu-id="db96d-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="db96d-128">Arrestare la riproduzione se il livello di protezione locale cambia in modo imprevisto o se viene rilevato un problema.</span><span class="sxs-lookup"><span data-stu-id="db96d-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db96d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db96d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db96d-130">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="db96d-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



