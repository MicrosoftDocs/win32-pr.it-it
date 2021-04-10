---
description: I log WinHTTP possono essere usati per risolvere i problemi delle applicazioni WSDAPI. Questa operazione è utile quando lo scambio di metadati ha esito negativo o quando la negoziazione SSL/TLS non riesce.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Acquisizione dei log WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131143"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="8aa8c-104">Acquisizione dei log WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8aa8c-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="8aa8c-105">I log [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) possono essere usati per risolvere i problemi delle applicazioni wsdapi.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="8aa8c-106">Questa operazione è utile quando lo scambio di metadati ha esito negativo o quando la negoziazione SSL/TLS non riesce.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="8aa8c-107">Questa procedura illustra come acquisire i log WinHTTP nel computer client.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="8aa8c-108">Quando è abilitata la registrazione, l'applicazione client basata su WSDAPI non deve essere in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="8aa8c-109">Se l'applicazione client è in esecuzione quando la registrazione è abilitata, il client e/o il PC devono essere riavviati prima che WS-Discovery e il traffico di scambio dei metadati venga visualizzato nei log WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="8aa8c-110">**Per acquisire i log WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="8aa8c-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="8aa8c-111">Aprire una finestra del prompt dei comandi con privilegi elevati nel computer client.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="8aa8c-112">Eseguire il comando seguente: **netsh winhttp set tracing trace-file-prefix = "C: \\ temp \\ DPWS" level = verbose Format = ANSI state = enabled max-trace-file-size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="8aa8c-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="8aa8c-113">Questo comando Abilita la registrazione WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="8aa8c-114">Tutti i file di log verranno archiviati nella directory C: \\ Temp e i nomi file inizieranno con il prefisso DPWS.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="8aa8c-115">Verranno archiviati al massimo 1 GB di file di log.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="8aa8c-116">Se il processo che usa WinHTTP sul client è già in esecuzione, riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="8aa8c-117">Se, ad esempio, vengono utilizzate le API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) , è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="8aa8c-118">Le API di individuazione della funzione chiamano WinHTTP dall'interno di un host del servizio, che potrebbe essere già stato avviato quando è stata abilitata la traccia.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="8aa8c-119">Avviare l'applicazione client basata su WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="8aa8c-120">L'applicazione di cui è in corso il debug o il client di debug WSD può essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="8aa8c-121">Riprodurre l'errore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="8aa8c-122">Terminare l'applicazione client basata su WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="8aa8c-123">Se il processo che usa WinHTTP non viene terminato con l'applicazione client, riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="8aa8c-124">Se, ad esempio, vengono utilizzate le API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) , è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="8aa8c-125">Eseguire il comando seguente: **netsh winhttp set tracing state = disabled**</span><span class="sxs-lookup"><span data-stu-id="8aa8c-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="8aa8c-126">Questo comando Disabilita la registrazione WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="8aa8c-127">Esaminare i registri di DPWS in C: \\ Temp e verificare che le richieste e i messaggi richiesti siano stati inviati.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="8aa8c-128">Se è in uso la comunicazione del canale sicuro (HTTPS), verificare la presenza di errori SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="8aa8c-129">Dopo l'acquisizione dei log WinHTTP, è possibile esaminare i log per cercare la cause di un errore dell'applicazione WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="8aa8c-130">Si noti che l'editor di testo utilizzato per visualizzare questi log deve essere eseguito come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8aa8c-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="8aa8c-131">Per altre informazioni, vedere [uso della registrazione WinHTTP per verificare il traffico](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="8aa8c-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aa8c-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8aa8c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aa8c-133">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8aa8c-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="8aa8c-134">Uso della registrazione WinHTTP per verificare il traffico Get</span><span class="sxs-lookup"><span data-stu-id="8aa8c-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
