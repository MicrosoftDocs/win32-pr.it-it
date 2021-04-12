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
# <a name="whats-new-in-wer"></a>Novità di WER

In questa pagina vengono riepilogate le nuove funzionalità di Segnalazione errori Windows (WER) per ogni versione.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Nell'elenco seguente sono riepilogate le nuove funzionalità di WER per Windows 7 e Windows Server 2008 R2.

-   Aggiunge la possibilità di generare un'eccezione che ignora tutti i gestori di eccezioni, terminando immediatamente l'applicazione e richiamando Segnalazione errori Windows. Per informazioni dettagliate, vedere la funzione [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .
-   Aggiunge la possibilità di registrare un gestore di eccezioni out-of-process che WER chiama quando si verifica un arresto anomalo per raccogliere il nome dell'evento, i parametri di report e le opzioni di avvio del debug. Per informazioni dettagliate, vedere la funzione [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .

Funzioni che sono state aggiunte:

-   [**OutOfProcessExceptionEventCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [**OutOfProcessExceptionEventSignatureCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [**OutOfProcessExceptionEventDebuggerLaunchCallback**](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))
-   [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [**WerUnregisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

Strutture aggiunte:

-   [**\_ \_ informazioni sulle eccezioni di runtime di wer \_**](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 e Windows Vista SP1

Nell'elenco seguente sono riepilogate le nuove funzionalità di WER per Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

-   WER può essere configurato in modo che i dump completi della modalità utente vengano raccolti e archiviati localmente dopo l'arresto anomalo di un'applicazione in modalità utente (le applicazioni che eseguono una segnalazione di arresti anomali personalizzata, incluse le applicazioni .NET non sono supportate). Per altre informazioni, vedere [collecting User-Mode dumps](collecting-user-mode-dumps.md).

## <a name="windows-vista"></a>Windows Vista

Nell'elenco seguente sono riepilogate le nuove funzionalità di Segnalazione errori Windows (WER) per Windows Vista:

-   WER è stato esteso oltre il monitoraggio degli arresti anomali e dei processi che non rispondono. WER include il supporto per molti nuovi tipi di eventi non critici, ad esempio problemi di prestazioni. Ciò consente agli sviluppatori di ottenere ulteriori informazioni sulle esperienze che i clienti hanno con le applicazioni sviluppate.
-   Le nuove funzioni offrono agli sviluppatori la flessibilità di creare, personalizzare e inviare report sui problemi. Per altre informazioni, vedere [funzioni wer](wer-functions.md).
-   Il miglioramento dei [servizi online di qualità Windows](https://www.microsoft.com/?ref=go) consente agli sviluppatori di accedere alle informazioni sui problemi che i clienti inviano per le proprie applicazioni e a un meccanismo per offrire soluzioni a questi clienti.
-   Le funzioni introdotte da [gestione](/windows/desktop/RstMgr/restart-manager-portal) [applicazioni e riavvio](/windows/desktop/Recovery/application-recovery-and-restart-portal) e riavvio consentono alle applicazioni di recuperare automaticamente le informazioni e di riavviarle in caso di errore critico. Gli sviluppatori possono usare queste funzionalità nelle applicazioni per migliorare significativamente l'esperienza utente.
-   **Segnalazioni di problemi e soluzioni in Windows Vista o centro operativo in Windows 7** è la posizione centrale in cui gli utenti possono interagire con wer. Gli utenti possono cercare nuove soluzioni, gestire la cronologia dei report, visualizzare i dettagli di un report sui problemi e gestire le impostazioni di Reporting, inclusa l'abilitazione di WER per verificare automaticamente la presenza di soluzioni senza interrompere l'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Segnalazione errori Windows](windows-error-reporting.md)
</dt> </dl>

 

 