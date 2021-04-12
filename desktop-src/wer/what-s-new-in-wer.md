---
title: Novità di WER
description: In questa pagina vengono riepilogate le nuove funzionalità di Segnalazione errori Windows (WER) per ogni versione.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Segnalazione errori Windows segnalazione errori Windows, novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336823"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="78047-104">Novità di WER</span><span class="sxs-lookup"><span data-stu-id="78047-104">What's New in WER</span></span>

<span data-ttu-id="78047-105">In questa pagina vengono riepilogate le nuove funzionalità di Segnalazione errori Windows (WER) per ogni versione.</span><span class="sxs-lookup"><span data-stu-id="78047-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="78047-106">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78047-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="78047-107">Nell'elenco seguente sono riepilogate le nuove funzionalità di WER per Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="78047-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="78047-108">Aggiunge la possibilità di generare un'eccezione che ignora tutti i gestori di eccezioni, terminando immediatamente l'applicazione e richiamando Segnalazione errori Windows.</span><span class="sxs-lookup"><span data-stu-id="78047-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="78047-109">Per informazioni dettagliate, vedere la funzione [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="78047-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="78047-110">Aggiunge la possibilità di registrare un gestore di eccezioni out-of-process che WER chiama quando si verifica un arresto anomalo per raccogliere il nome dell'evento, i parametri di report e le opzioni di avvio del debug.</span><span class="sxs-lookup"><span data-stu-id="78047-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="78047-111">Per informazioni dettagliate, vedere la funzione [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .</span><span class="sxs-lookup"><span data-stu-id="78047-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="78047-112">Funzioni che sono state aggiunte:</span><span class="sxs-lookup"><span data-stu-id="78047-112">Functions that were added:</span></span>

-   [<span data-ttu-id="78047-113">**OutOfProcessExceptionEventCallback**</span><span class="sxs-lookup"><span data-stu-id="78047-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="78047-114">**OutOfProcessExceptionEventSignatureCallback**</span><span class="sxs-lookup"><span data-stu-id="78047-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="78047-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span><span class="sxs-lookup"><span data-stu-id="78047-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="78047-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78047-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="78047-117">**WerRegisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="78047-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="78047-118">**WerUnregisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="78047-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="78047-119">Strutture aggiunte:</span><span class="sxs-lookup"><span data-stu-id="78047-119">Structures that were added:</span></span>

-   [<span data-ttu-id="78047-120">**\_ \_ informazioni sulle eccezioni di runtime di wer \_**</span><span class="sxs-lookup"><span data-stu-id="78047-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="78047-121">Windows Server 2008 e Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="78047-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="78047-122">Nell'elenco seguente sono riepilogate le nuove funzionalità di WER per Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="78047-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="78047-123">WER può essere configurato in modo che i dump completi della modalità utente vengano raccolti e archiviati localmente dopo l'arresto anomalo di un'applicazione in modalità utente (le applicazioni che eseguono una segnalazione di arresti anomali personalizzata, incluse le applicazioni .NET non sono supportate).</span><span class="sxs-lookup"><span data-stu-id="78047-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="78047-124">Per altre informazioni, vedere [collecting User-Mode dumps](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="78047-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="78047-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78047-125">Windows Vista</span></span>

<span data-ttu-id="78047-126">Nell'elenco seguente sono riepilogate le nuove funzionalità di Segnalazione errori Windows (WER) per Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="78047-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="78047-127">WER è stato esteso oltre il monitoraggio degli arresti anomali e dei processi che non rispondono.</span><span class="sxs-lookup"><span data-stu-id="78047-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="78047-128">WER include il supporto per molti nuovi tipi di eventi non critici, ad esempio problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="78047-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="78047-129">Ciò consente agli sviluppatori di ottenere ulteriori informazioni sulle esperienze che i clienti hanno con le applicazioni sviluppate.</span><span class="sxs-lookup"><span data-stu-id="78047-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="78047-130">Le nuove funzioni offrono agli sviluppatori la flessibilità di creare, personalizzare e inviare report sui problemi.</span><span class="sxs-lookup"><span data-stu-id="78047-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="78047-131">Per altre informazioni, vedere [funzioni wer](wer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="78047-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="78047-132">Il miglioramento dei [servizi online di qualità Windows](https://www.microsoft.com/?ref=go) consente agli sviluppatori di accedere alle informazioni sui problemi che i clienti inviano per le proprie applicazioni e a un meccanismo per offrire soluzioni a questi clienti.</span><span class="sxs-lookup"><span data-stu-id="78047-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="78047-133">Le funzioni introdotte da [gestione](/windows/desktop/RstMgr/restart-manager-portal) [applicazioni e riavvio](/windows/desktop/Recovery/application-recovery-and-restart-portal) e riavvio consentono alle applicazioni di recuperare automaticamente le informazioni e di riavviarle in caso di errore critico.</span><span class="sxs-lookup"><span data-stu-id="78047-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="78047-134">Gli sviluppatori possono usare queste funzionalità nelle applicazioni per migliorare significativamente l'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="78047-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="78047-135">**Segnalazioni di problemi e soluzioni in Windows Vista o centro operativo in Windows 7** è la posizione centrale in cui gli utenti possono interagire con wer.</span><span class="sxs-lookup"><span data-stu-id="78047-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="78047-136">Gli utenti possono cercare nuove soluzioni, gestire la cronologia dei report, visualizzare i dettagli di un report sui problemi e gestire le impostazioni di Reporting, inclusa l'abilitazione di WER per verificare automaticamente la presenza di soluzioni senza interrompere l'utente.</span><span class="sxs-lookup"><span data-stu-id="78047-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78047-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78047-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78047-138">Segnalazione errori Windows</span><span class="sxs-lookup"><span data-stu-id="78047-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 