---
description: Uso di COPP (Certified Output Protocol)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Uso di COPP (Certified Output Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314398"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="1b868-103">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="1b868-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="1b868-104">Certified Output Protection Protocol (COPP) consente a un'applicazione di proteggere un flusso video mentre passa dalla scheda grafica al dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b868-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="1b868-105">Un'applicazione può usare COPP per individuare il tipo di connettore fisico collegato al dispositivo di visualizzazione e i tipi di protezione dell'output disponibili.</span><span class="sxs-lookup"><span data-stu-id="1b868-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="1b868-106">Tra i meccanismi di protezione sono inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b868-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="1b868-107">High-Bandwidth protezione del contenuto digitali (HDCP)</span><span class="sxs-lookup"><span data-stu-id="1b868-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="1b868-108">Sistema di gestione della generazione di copia: analogico (CGMS-A)</span><span class="sxs-lookup"><span data-stu-id="1b868-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="1b868-109">Protezione copia analogica (ACP)</span><span class="sxs-lookup"><span data-stu-id="1b868-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="1b868-110">Se la scheda grafica supporta uno di questi meccanismi, l'applicazione può utilizzare COPP per impostare il livello di protezione.</span><span class="sxs-lookup"><span data-stu-id="1b868-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="1b868-111">COPP definisce un protocollo usato per stabilire un canale di comunicazione sicuro con il driver di grafica.</span><span class="sxs-lookup"><span data-stu-id="1b868-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="1b868-112">USA i codici Mac (Message Authentication Code) per verificare l'integrità dei comandi COPP passati tra l'applicazione e il driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b868-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="1b868-113">L'applicazione usa COPP chiamando i metodi sull'interfaccia [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) del filtro renderer video mixing (VMR-7 o VMR-9).</span><span class="sxs-lookup"><span data-stu-id="1b868-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="1b868-114">COPP non definisce informazioni sui criteri per i diritti digitali che possono essere applicati al contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="1b868-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="1b868-115">Inoltre, COPP non implementa alcun sistema di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="1b868-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="1b868-116">Il protocollo COPP fornisce semplicemente un modo per impostare ed eseguire query sui livelli di protezione sulla scheda grafica, usando i sistemi di protezione forniti dall'adapter.</span><span class="sxs-lookup"><span data-stu-id="1b868-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="1b868-117">In questa sezione si presuppone che l'utente abbia familiarità con le tecnologie seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b868-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="1b868-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b868-118">DirectShow</span></span>
-   <span data-ttu-id="1b868-119">Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="1b868-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="1b868-120">XML</span><span class="sxs-lookup"><span data-stu-id="1b868-120">XML</span></span>
-   <span data-ttu-id="1b868-121">Crittografia a chiave pubblica e crittografia simmetrica</span><span class="sxs-lookup"><span data-stu-id="1b868-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="1b868-122">Negli esempi di codice di questa sezione viene utilizzato CryptoAPI di Microsoft per eseguire operazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1b868-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="1b868-123">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="1b868-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1b868-124">Panoramica di COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="1b868-125">Recupero della catena di certificati del driver</span><span class="sxs-lookup"><span data-stu-id="1b868-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="1b868-126">Convalida della catena di certificati</span><span class="sxs-lookup"><span data-stu-id="1b868-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="1b868-127">Elenchi di revoche dei certificati</span><span class="sxs-lookup"><span data-stu-id="1b868-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="1b868-128">Importazione della chiave pubblica del driver</span><span class="sxs-lookup"><span data-stu-id="1b868-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="1b868-129">Avvio di una sessione COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="1b868-130">Invio di richieste di stato di COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="1b868-131">Invio di comandi COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="1b868-132">Verifica se un driver di grafica supporta COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="1b868-133">Riferimento alla query COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="1b868-134">Riferimento al comando COPP</span><span class="sxs-lookup"><span data-stu-id="1b868-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="1b868-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b868-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b868-136">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="1b868-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



