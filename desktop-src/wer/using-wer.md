---
title: Uso di WER
description: A partire da Windows Vista, Windows fornisce la segnalazione di errori di arresto anomalo, di non risposta e del kernel, per impostazione predefinita senza richiedere modifiche all'applicazione.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Segnalazione errori Windows Segnalazione errori Windows, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bed6d11757d7d4e08cd00ac47479e1246f96b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104398842"
---
# <a name="using-wer"></a>Uso di WER

A partire da Windows Vista, Windows fornisce la segnalazione di errori di arresto anomalo, di non risposta e del kernel, per impostazione predefinita senza richiedere modifiche all'applicazione. Se necessario, il report includerà i minidump e le informazioni sul dump dell'heap. Le applicazioni usano invece l'API WER per inviare segnalazioni di problemi specifici dell'applicazione a Microsoft.

Poiché Windows segnala automaticamente le eccezioni non gestite, l'applicazione non deve gestire le eccezioni irreversibili. Se il processo di errore o non risposta è interattivo, WER Visualizza un'interfaccia utente che informa l'utente del problema. Un'applicazione è considerata non risponde se non risponde ai messaggi di Windows per cinque secondi mentre l'utente tenta di interagire con l'applicazione.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Flusso di Segnalazione errori Windows per arresti anomali, non di risposta e errori del kernel

Di seguito vengono illustrati i passaggi che si verificano per l'arresto anomalo dell'applicazione, la mancata risposta o l'errore del kernel.

1.  Si è verificato l'evento relativo al problema.
2.  Il sistema operativo richiama WER.
3.  WER raccoglie i dati, compila un report e richiede il consenso dell'utente (se necessario).
4.  WER invia il report a Microsoft (server Watson) se l'utente ha acconsentito.
5.  Se il server Watson richiede dati aggiuntivi, WER raccoglie i dati e chiede all'utente il consenso (se necessario).
6.  Se l'applicazione è stata registrata per il ripristino e il riavvio, WER esegue le funzioni di callback registrate mentre i dati vengono compressi e inviati a Microsoft, se l'utente ha acconsentito.
7.  Se una risposta al problema è disponibile da Microsoft, l'utente riceve una notifica.

Le applicazioni possono utilizzare le seguenti funzioni per personalizzare il contenuto del report inviato a Microsoft. Le funzioni di registrazione indicano a WER di includere i file e i blocchi di memoria specifici nella segnalazione degli errori creata.

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Flusso di Segnalazione errori Windows per la segnalazione di eventi generici

Nei passaggi seguenti viene illustrato il modo in cui le applicazioni possono ottenere una segnalazione errori per una condizione di errore non irreversibile.

1.  Si verifica l'evento di problema non irreversibile.
2.  L'applicazione riconosce l'evento e utilizza la seguente sequenza di chiamate di funzione per generare il report.
    1.  Chiamare la funzione [**WerReportCreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) per creare il report.
    2.  Chiamare la funzione [**WerReportSetParameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) per impostare i parametri del report.
    3.  Chiamare la funzione [**WerReportAddFile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) per aggiungere file al report.
    4.  Chiamare la funzione [**WerReportAddDump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) per aggiungere un minidump al report, se necessario.
    5.  Chiamare la funzione [**WerReportSubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) per inviare il report.
    6.  Chiamare [**WerReportCloseHandle**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) per liberare risorse.
3.  A seconda delle opzioni specifiche utilizzate quando si chiamano le funzioni nel passaggio 2, WER completerà la segnalazione degli errori. WER garantisce che la creazione di report venga eseguita in base ai criteri impostati dall'utente. Ad esempio, WER invierà il report a Microsoft, Accoda il report e visualizzerà le interfacce utente appropriate per l'utente.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Esclusione di un'applicazione da Segnalazione errori Windows

Per escludere l'applicazione da segnalazione errori Windows, utilizzare la funzione [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) . Per ripristinare la segnalazione degli errori per l'applicazione, utilizzare la funzione [**WerRemoveExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication) .

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Ripristino automatico dei dati e riavvio di un'applicazione con errori

Un'applicazione può usare il ripristino e il riavvio dell'applicazione per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere. Se richiesto, viene riavviata anche l'applicazione. Per informazioni dettagliate, vedere [ripristino dell'applicazione e riavvio](/windows/desktop/Recovery/application-recovery-and-restart-portal).

## <a name="legacy-api"></a>API legacy

Un'applicazione può segnalare un errore chiamando la funzione [**ReportFault**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) . Tuttavia, non è consigliabile usare la funzione **ReportFault** , a meno che non si disponga di un requisito molto specifico che il comportamento predefinito di segnalazione errori del sistema operativo non possa essere completato.

Se la segnalazione errori è abilitata, viene visualizzata una finestra di dialogo che indica che l'applicazione ha riscontrato un problema e si chiuderà. Se è presente un debugger configurato nella **HKEY della \_ chiave \_ \\ \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AeDebug del software del computer locale** , all'utente viene assegnata l'opzione per avviare il debugger. All'utente viene inoltre offerta la possibilità di inviare un report a Microsoft. Se l'utente invia il report, viene visualizzata un'altra finestra di dialogo che ringrazia l'utente per il report e fornisce un collegamento a ulteriori informazioni.

Il sistema di segnalazione degli errori supporta le modalità operative seguenti.



| Modalità operativa          | Descrizione                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Segnalazione memoria condivisa | Se il contesto di sicurezza dell'applicazione è lo stesso del contesto di sicurezza dell'utente connesso, il sistema di segnalazione degli errori utilizza un blocco di memoria condivisa per la comunicazione. Questa modalità non può essere utilizzata con la modalità di creazione rapporti manifesto.<br/>                                                                                               |
| Creazione di report manifesto      | Se il contesto di sicurezza dell'applicazione non corrisponde al contesto di sicurezza dell'utente connesso, il sistema di segnalazione degli errori utilizza un file per la comunicazione. Questa modalità viene usata anche per segnalare le applicazioni che non rispondono e gli errori del kernel. Questa modalità non può essere utilizzata con la modalità di segnalazione memoria condivisa.<br/>                      |
| Segnalazione Internet      | Il sistema di segnalazione degli errori invia tutti i dati a Microsoft attraverso Internet. Questa è la modalità operativa predefinita. Non può essere utilizzato con la modalità di creazione di report aziendale. Questa modalità viene usata in assenza di un percorso di caricamento aziendale specificato dall'amministratore.<br/>                                                                     |
| Creazione di report aziendali     | Il sistema di segnalazione degli errori invia tutti i dati a una condivisione file anziché caricarli direttamente in Microsoft. Ciò consente ai responsabili IT aziendali di esaminare i dati prima che vengano inviati a Microsoft. Questa modalità viene usata quando è presente un percorso di caricamento aziendale specificato dall'amministratore. Non può essere utilizzato con la modalità di segnalazione Internet.<br/> |
| Creazione di report      | Nel sistema di segnalazione degli errori non verrà visualizzata alcuna finestra di dialogo. Ciò consente ai responsabili IT aziendali di raccogliere in qualsiasi momento le segnalazioni degli errori dai propri dipendenti. Questa modalità viene utilizzata quando la creazione di report viene abilitata dall'amministratore, ma la notifica è disabilitata. Può essere usato solo con la modalità di creazione di report aziendale.<br/>        |



 

Per escludere l'applicazione dalla segnalazione errori, usare la funzione [**AddERExcludedApplication**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa) .

 

