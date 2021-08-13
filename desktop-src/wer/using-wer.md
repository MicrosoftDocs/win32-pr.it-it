---
title: Uso di WER
description: A partire da Windows Vista, Windows la segnalazione degli errori di arresto anomalo, non di risposta e kernel per impostazione predefinita senza richiedere modifiche all'applicazione.
ms.assetid: c096cd89-e3a7-4959-a35f-40e6168f277e
keywords:
- Windows segnalazione errori Segnalazione errori Windows , tramite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dfa8bc2235f43770cd177ad3e5d9a7d1aacde36034152b88cb06af3879e8c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442241"
---
# <a name="using-wer"></a>Uso di WER

A partire da Windows Vista, Windows la segnalazione degli errori di arresto anomalo, non di risposta e kernel per impostazione predefinita senza richiedere modifiche all'applicazione. Il report includerà minidump e informazioni sul dump dell'heap, se necessario. Le applicazioni usano invece l'API WER per inviare segnalazioni di problemi specifiche dell'applicazione a Microsoft.

Poiché Windows segnala automaticamente eccezioni non gestite, l'applicazione non deve gestire le eccezioni irreversibili. Se il processo di errore o non risponde è interattivo, WER visualizza un'interfaccia utente che informa l'utente del problema. Un'applicazione viene considerata non risponde se non risponde Windows messaggi per cinque secondi mentre l'utente tenta di interagire con l'applicazione.

## <a name="windows-error-reporting-flow-for-crashes-non-response-and-kernel-faults"></a>Segnalazione errori Windows flusso per arresti anomali, non risposta e errori del kernel

Di seguito sono illustrati i passaggi che si verificano per un arresto anomalo dell'applicazione, una mancata risposta o un errore del kernel.

1.  Si verifica l'evento di problema.
2.  Il sistema operativo richiama WER.
3.  WER raccoglie i dati, compila un report e richiede il consenso dell'utente (se necessario).
4.  WER invia il report a Microsoft (Server Watson) se l'utente ha acconsentito.
5.  Se il server Watson richiede dati aggiuntivi, WER raccoglie i dati e richiede all'utente il consenso (se necessario).
6.  Se l'applicazione è stata registrata per il ripristino e il riavvio, WER esegue le funzioni di callback registrate mentre i dati vengono compressi e inviati a Microsoft (se l'utente ha acconsentito).
7.  Se è disponibile una risposta al problema da Microsoft, l'utente viene informato.

Le applicazioni possono usare le funzioni seguenti per personalizzare il contenuto del report inviato a Microsoft. Le funzioni di registrazione segnalano a WER di includere i file e i blocchi di memoria specifici nella segnalazione errori creata.

-   [**WerRegisterFile**](/windows/desktop/api/Werapi/nf-werapi-werregisterfile)
-   [**WerRegisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werregistermemoryblock)
-   [**WerSetFlags**](/windows/desktop/api/Werapi/nf-werapi-wersetflags)
-   [**WerUnregisterFile**](/windows/desktop/api/Werapi/nf-werapi-werunregisterfile)
-   [**WerUnregisterMemoryBlock**](/windows/desktop/api/Werapi/nf-werapi-werunregistermemoryblock)
-   [**WerGetFlags**](/windows/desktop/api/Werapi/nf-werapi-wergetflags)

## <a name="windows-error-reporting-flow-for-generic-event-reporting"></a>Segnalazione errori Windows flusso per la creazione di report di eventi generici

La procedura seguente illustra come le applicazioni possono ottenere una segnalazione errori per una condizione di errore non irreversibile.

1.  Si verifica l'evento di problema non irreversibile.
2.  L'applicazione riconosce l'evento e usa la sequenza di chiamate di funzione seguente per generare il report.
    1.  Chiamare la [**funzione WerReportCreate**](/windows/desktop/api/Werapi/nf-werapi-werreportcreate) per creare il report.
    2.  Chiamare la [**funzione WerReportSetParameter**](/windows/desktop/api/Werapi/nf-werapi-werreportsetparameter) per impostare i parametri del report.
    3.  Chiamare la [**funzione WerReportAddFile**](/windows/desktop/api/Werapi/nf-werapi-werreportaddfile) per aggiungere file al report.
    4.  Chiamare la [**funzione WerReportAddDump**](/windows/desktop/api/Werapi/nf-werapi-werreportadddump) per aggiungere un minidump al report (se necessario).
    5.  Chiamare la [**funzione WerReportSubmit**](/windows/desktop/api/Werapi/nf-werapi-werreportsubmit) per inviare il report.
    6.  Chiamare [**WerReportCloseHandle per**](/windows/desktop/api/Werapi/nf-werapi-werreportclosehandle) liberare risorse.
3.  A seconda delle opzioni specifiche usate quando si chiamano le funzioni nel passaggio 2, WER terminerà la segnalazione degli errori. WeR garantisce che la creazione di report sia eseguita in base ai criteri impostati dall'utente. Ad esempio, WER invierà il report a Microsoft, accoderà il report e mostrerà le interfacce utente appropriate all'utente.

## <a name="excluding-an-application-from-windows-error-reporting"></a>Esclusione di un'applicazione da Segnalazione errori Windows

Per escludere l'applicazione Windows segnalazione errori, usare la [**funzione WerAddExcludedApplication.**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication) Per ripristinare la segnalazione degli errori per l'applicazione, usare [**la funzione WerRemoveExcludedApplication.**](/windows/desktop/api/Werapi/nf-werapi-werremoveexcludedapplication)

## <a name="automatically-recovering-data-and-restarting-a-faulted-application"></a>Ripristino automatico dei dati e riavvio di un'applicazione con errori

Un'applicazione può usare Ripristino applicazioni e Riavvia per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere. Anche l'applicazione viene riavviata, se richiesto. Per informazioni dettagliate, vedere [Ripristino applicazioni e riavvio.](/windows/desktop/Recovery/application-recovery-and-restart-portal)

## <a name="legacy-api"></a>Legacy API

Un'applicazione può segnalare un errore chiamando la [**funzione ReportFault.**](/windows/desktop/api/ErrorRep/nf-errorrep-reportfault) Tuttavia, non è consigliabile usare la **funzione ReportFault** a meno che non si abbia un requisito molto specifico che il comportamento di segnalazione degli errori predefinito del sistema operativo non può soddisfare.

Se la segnalazione errori è abilitata, il sistema visualizza una finestra di dialogo per l'utente che indica che l'applicazione ha rilevato un problema e verrà chiusa. Se è presente un debugger configurato nella chiave **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ AeDebug,** all'utente viene data la possibilità di avviare il debugger. All'utente viene anche data la possibilità di inviare un report a Microsoft. Se l'utente invia il report, il sistema visualizza un'altra finestra di dialogo che ringrazia l'utente per il report e fornisce un collegamento a altre informazioni.

Il sistema di segnalazione errori supporta le modalità operative seguenti.



| Modalità operazione          | Descrizione                                                                                                                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creazione di report sulla memoria condivisa | Se il contesto di sicurezza dell'applicazione è lo stesso del contesto di sicurezza dell'utente connesso, il sistema di segnalazione errori usa un blocco di memoria condivisa per la comunicazione. Questa modalità non può essere usata con la modalità di creazione di report del manifesto.<br/>                                                                                               |
| Creazione di report dei manifesti      | Se il contesto di sicurezza dell'applicazione non corrisponde al contesto di sicurezza dell'utente connesso, il sistema di segnalazione errori usa un file per la comunicazione. Questa modalità viene usata anche per la segnalazione di applicazioni non rispondenti ed errori del kernel. Questa modalità non può essere usata con la modalità di creazione di report della memoria condivisa.<br/>                      |
| Creazione di report Internet      | Il sistema di segnalazione errori invia tutti i dati a Microsoft tramite Internet. Questa è la modalità operativa predefinita. Non può essere usato con la modalità di creazione report aziendale. Questa modalità viene usata quando l'amministratore non ha specificato alcun percorso di caricamento aziendale.<br/>                                                                     |
| Creazione di report aziendali     | Il sistema di segnalazione errori invia tutti i dati a una condivisione file anziché caricarlo direttamente a Microsoft. In questo modo i responsabili IT aziendali possono esaminare i dati prima di essere inviati a Microsoft. Questa modalità viene usata quando l'amministratore ha specificato un percorso di caricamento aziendale. Non può essere usato con la modalità di creazione report Internet.<br/> |
| Creazione di report headless      | Il sistema di segnalazione errori non visualizza alcuna finestra di dialogo per l'utente. In questo modo i responsabili IT aziendali possono raccogliere in qualsiasi momento le segnalazioni degli errori dei dipendenti. Questa modalità viene usata quando la creazione di report è abilitata dall'amministratore, ma la notifica è disabilitata. Può essere usato solo con la modalità di creazione report aziendale.<br/>        |



 

Per escludere l'applicazione dalla segnalazione errori, usare la [**funzione AddERExcludedApplication.**](/windows/desktop/api/ErrorRep/nf-errorrep-adderexcludedapplicationa)

 

