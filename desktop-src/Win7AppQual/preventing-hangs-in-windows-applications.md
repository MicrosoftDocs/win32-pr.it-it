---
description: Informazioni su come evitare blocchi nelle applicazioni Windows per le piattaforme Windows 7 e Windows Server 2008 R2.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Prevenzione di blocchi nelle applicazioni Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a2d8fac95039f20c8c684c50138933c54750c3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104058408"
---
# <a name="preventing-hangs-in-windows-applications"></a>Prevenzione di blocchi nelle applicazioni Windows

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="description"></a>Descrizione

**Blocchi-prospettiva utente**

Utenti come le applicazioni reattive. Quando si fa clic su un menu, si desidera che l'applicazione reagisca immediatamente, anche se attualmente sta stampando il lavoro. Quando si salva un documento lungo nel proprio elaboratore di testo preferito, è necessario continuare a digitare mentre il disco è ancora in fase di rotazione. Gli utenti si impazienteno piuttosto rapidamente quando l'applicazione non reagirà tempestivamente all'input.

Un programmatore potrebbe riconoscere molti motivi legittimi per cui un'applicazione non risponde immediatamente all'input dell'utente. È possibile che l'applicazione sia occupata per il ricalcolo di alcuni dati o semplicemente in attesa del completamento dell'I/O del disco. Tuttavia, dalla ricerca degli utenti, sappiamo che gli utenti si annoiano e sono frustrati dopo un paio di secondi di inattività. Dopo 5 secondi tenterà di terminare un'applicazione bloccata. Accanto a arresti anomali, i blocchi dell'applicazione sono l'origine più comune di interruzioni dell'utente quando si lavora con le applicazioni Win32.

Ci sono molte cause principali diverse per i blocchi dell'applicazione e non tutti si manifestano in un'interfaccia utente che non risponde. Tuttavia, un'interfaccia utente che non risponde è una delle più comuni esperienze di blocco e questo scenario attualmente riceve la maggior parte del supporto del sistema operativo sia per il rilevamento che per il ripristino. Windows rileva automaticamente, raccoglie le informazioni di debug e, facoltativamente, termina o riavvia le applicazioni appese. In caso contrario, l'utente potrebbe dover riavviare il computer per ripristinare un'applicazione bloccata.

**Blocchi-prospettiva del sistema operativo**

Quando un'applicazione (o più accuratamente, un thread) crea una finestra sul desktop, entra in un contratto implicito con il Gestione finestre desktop (DWM) per elaborare i messaggi della finestra in modo tempestivo. DWM inserisce i messaggi (input da tastiera/mouse e messaggi da altre finestre, così come se stessi) nella coda di messaggi specifica del thread. Il thread recupera e invia tali messaggi tramite la relativa coda di messaggi. Se il thread non esegue la manutenzione della coda chiamando GetMessage (), i messaggi non vengono elaborati e la finestra si blocca: non può né ridisegnato né può accettare l'input dell'utente. Il sistema operativo rileva questo stato connettendo un timer ai messaggi in sospeso nella coda di messaggi. Se un messaggio non è stato recuperato entro 5 secondi, DWM dichiara che la finestra deve essere bloccata. È possibile eseguire query su questo particolare stato della finestra tramite l'API IsHungAppWindow ().

Il rilevamento è solo il primo passaggio. A questo punto, l'utente non può ancora terminare l'applicazione. Se si fa clic sul pulsante X (Chiudi), \_ verrà visualizzato un messaggio di chiusura WM, che verrebbe bloccato nella coda dei messaggi esattamente come per qualsiasi altro messaggio. Il Gestione finestre desktop facilita la semplice occultamento e la sostituzione della finestra bloccata con una copia ' fantasma ' che visualizza una bitmap dell'area client precedente della finestra originale (e l'aggiunta di "non risponde" alla barra del titolo). Finché il thread della finestra originale non recupera i messaggi, DWM gestisce entrambe le finestre simultaneamente, ma consente all'utente di interagire solo con la copia fantasma. Utilizzando questa finestra fantasma, l'utente può solo spostare, ridurre a icona e, più importante, chiudere l'applicazione che non risponde, ma non modificarne lo stato interno.

L'intera esperienza fantasma ha un aspetto simile al seguente:

![Screenshot che mostra la finestra di dialogo "blocco note non risponde".](images/preventinghangs-ghostwindow.gif)

Il Gestione finestre desktop esegue un'ultima operazione; si integra con Segnalazione errori Windows, consentendo all'utente non solo di chiudere e, facoltativamente, di riavviare l'applicazione, ma anche di inviare dati di debug importanti a Microsoft. Puoi ottenere questi dati di blocco per le tue applicazioni iscrivendoti al sito Web winqual.

Windows 7 ha aggiunto una nuova funzionalità a questa esperienza. Il sistema operativo analizza l'applicazione bloccata e, in determinate circostanze, offre all'utente la possibilità di annullare un'operazione di blocco e di riattivare l'applicazione. L'implementazione corrente supporta l'annullamento delle chiamate al socket di blocco; altre operazioni saranno annullabili dall'utente nelle versioni future.

Per integrare l'applicazione con l'esperienza di ripristino del blocco e per sfruttare al meglio i dati disponibili, attenersi alla procedura seguente:

-   Assicurarsi che l'applicazione venga registrata per il riavvio e il ripristino, facendo in modo che un blocco sia più libero possibile per l'utente. Un'applicazione registrata correttamente può essere riavviata automaticamente con la maggior parte dei dati non salvati intatti. Questa operazione può essere eseguita per blocchi e arresti anomali dell'applicazione.
-   Ottenere informazioni sulla frequenza, nonché i dati di debug per le applicazioni bloccate e bloccate dal sito Web winqual. È possibile usare queste informazioni anche durante la beta per migliorare il codice. Per una breve panoramica, vedere "Introduzione a Segnalazione errori Windows".
-   È possibile disabilitare la funzionalità ghosting nell'applicazione tramite una chiamata a DisableProcessWindowsGhosting (). Tuttavia, in questo modo si impedisce all'utente medio di chiudere e riavviare un'applicazione bloccata e spesso termina con un riavvio.

**Blocchi-prospettiva per sviluppatori**

Il sistema operativo definisce un'applicazione bloccata come un thread dell'interfaccia utente che non ha elaborato i messaggi per almeno 5 secondi. I bug evidenti provocano alcuni blocchi, ad esempio un thread in attesa di un evento che non viene mai segnalato e due thread che bloccano e tentano di acquisire gli altri. È possibile correggere i bug senza troppi sforzi. Tuttavia, molti blocchi non sono così chiari. Sì, il thread dell'interfaccia utente non recupera i messaggi, ma è ugualmente occupato a eseguire altre attività "importanti" e alla fine verrà restituito l'elaborazione dei messaggi.

Tuttavia, l'utente lo percepisce come un bug. Il progetto deve corrispondere alle aspettative dell'utente. Se la progettazione dell'applicazione conduce a un'applicazione che non risponde, sarà necessario modificare la progettazione. Infine, e questo è importante, la mancata risposta non può essere fissata come un bug del codice; richiede un lavoro iniziale durante la fase di progettazione. Il tentativo di adattare la codebase esistente di un'applicazione per rendere l'interfaccia utente più reattiva è spesso troppo costosa. Le linee guida di progettazione seguenti potrebbero essere utili.

-   Rendere la velocità di risposta dell'interfaccia utente un requisito di livello superiore; l'utente deve sempre tenere sotto controllo l'applicazione
-   Assicurarsi che gli utenti possano annullare le operazioni che importano più di un secondo per il completamento e/o che le operazioni possano essere completate in background; fornire l'interfaccia utente di avanzamento appropriata, se necessario

![Screenshot che mostra la finestra di dialogo "copia di elementi".](images/preventinghangs-progressbar.gif)

-   Accodare operazioni a esecuzione prolungata o bloccate come attività in background (questo richiede un meccanismo di messaggistica ben concepito per informare il thread dell'interfaccia utente quando il lavoro è stato completato)
-   Mantieni semplice il codice per i thread dell'interfaccia utente; rimuovere il maggior numero possibile di chiamate API di blocco
-   Mostra finestre e finestre di dialogo solo quando sono pronte e completamente operative. Se la finestra di dialogo deve visualizzare informazioni che richiedono un utilizzo eccessivo delle risorse per il calcolo, visualizzare prima alcune informazioni generiche e aggiornarle immediatamente quando diventano disponibili più dati. Un esempio valido è la finestra di dialogo Proprietà cartella da Esplora risorse. Deve visualizzare le dimensioni totali della cartella, le informazioni che non sono immediatamente disponibili dal file system. La finestra di dialogo viene visualizzata immediatamente e il campo "size" viene aggiornato da un thread di lavoro:

![Screenshot che mostra la pagina generale delle proprietà di Windows con il testo "size", "size on disk" e "Contains".](images/preventinghangs-updatingdialog.gif)

Sfortunatamente, non esiste un modo semplice per progettare e scrivere un'applicazione reattiva. Windows non fornisce un semplice Framework asincrono che consente una pianificazione semplice del blocco o di operazioni con esecuzione prolungata. Le sezioni seguenti introducono alcune delle procedure consigliate per prevenire i blocchi ed evidenziare alcuni problemi comuni.

## <a name="best-practices"></a>Procedure consigliate

**Mantieni semplice il thread dell'interfaccia utente**

La responsabilità principale del thread dell'interfaccia utente è recuperare e inviare messaggi. Qualsiasi altro tipo di lavoro introduce il rischio di appendere le finestre di proprietà del thread.

**Fare**

-   Spostare algoritmi a elevato utilizzo di risorse o non associati che comportano operazioni a esecuzione prolungata ai thread di lavoro
-   Identificare il numero di chiamate di funzione di blocco possibili e provare a spostarle nei thread di lavoro; qualsiasi funzione che chiama un'altra DLL dovrebbe essere sospetta
-   Eseguire un'operazione aggiuntiva per rimuovere tutte le chiamate API di I/O di file e di rete dal thread di lavoro. Queste funzioni possono bloccarsi per molti secondi se non sono minuti. Se è necessario eseguire qualsiasi tipo di I/O nel thread UI, provare a usare l'I/O asincrono
-   Tenere presente che il thread dell'interfaccia utente è anche in grado di gestire tutti i server COM di Apartment a thread singolo (STA) ospitati dal processo. Se si effettua una chiamata di blocco, questi server COM non risponderanno fino a quando non si riservirà la coda dei messaggi

**Non:**

-   Attendere qualsiasi oggetto kernel, ad esempio Event o mutex, per un periodo di tempo molto breve; Se è necessario attendere, provare a usare MsgWaitForMultipleObjects (), che si sblocca quando arriva un nuovo messaggio
-   Condividere la coda di messaggi della finestra di un thread con un altro thread utilizzando la funzione AttachThreadInput (). Non è solo estremamente difficile sincronizzare correttamente l'accesso alla coda, ma anche impedire al sistema operativo Windows di rilevare correttamente una finestra bloccata
-   Usare TerminateThread () in uno qualsiasi dei thread di lavoro. La chiusura di un thread in questo modo non consentirà di rilasciare i blocchi o gli eventi di segnale e può facilmente produrre oggetti di sincronizzazione orfani
-   Chiama il codice ' Unknown ' dal thread dell'interfaccia utente. Ciò è particolarmente vero se l'applicazione ha un modello di estendibilità. non vi è alcuna garanzia che il codice di terze parti segua le linee guida per la velocità di risposta
-   Eseguire qualsiasi tipo di chiamata di trasmissione di blocco; SendMessage ( \_ trasmissione HWND) si pone alla mercé di ogni applicazione attualmente in esecuzione

**Implementare i modelli asincroni**

La rimozione di operazioni a esecuzione prolungata o di blocco dal thread UI richiede l'implementazione di un Framework asincrono che consente di eseguire l'offload di tali operazioni ai thread di lavoro.

**Fare**

-   Usare le API dei messaggi di finestra asincrone nel thread dell'interfaccia utente, in particolare sostituendo SendMessage con uno dei relativi peer non bloccanti: PostMessage, SendNotifyMessage o SendMessageCallback
-   Usare i thread in background per eseguire attività a esecuzione prolungata o di blocco. Usare la nuova API del pool di thread per implementare i thread di lavoro
-   Fornire il supporto per l'annullamento per le attività in background con esecuzione prolungata. Per le operazioni di I/O di blocco, utilizzare l'annullamento I/O, ma solo come ultima risorsa. non è facile annullare l'operazione "Right"
-   Implementare una progettazione asincrona per il codice gestito usando il modello IAsyncResult o gli eventi

**Usare i blocchi in modo oculato**

L'applicazione o la DLL necessita di blocchi per sincronizzare l'accesso alle strutture di dati interne. L'uso di più blocchi aumenta il parallelismo e rende l'applicazione più reattiva. Tuttavia, l'utilizzo di più blocchi aumenta anche la possibilità di acquisire tali blocchi in ordini diversi e causare il deadlock dei thread. Se due thread contengono un blocco e tentano di acquisire il blocco del altro thread, le relative operazioni costituiranno un'attesa circolare che blocca lo stato di avanzamento di questi thread. È possibile evitare questo deadlock solo assicurandosi che tutti i thread dell'applicazione acquisiscano sempre tutti i blocchi nello stesso ordine. Tuttavia, non è sempre facile acquisire i blocchi nell'ordine "corretto". È possibile comporre componenti software, ma le acquisizioni di blocchi non possono. Se il codice chiama un altro componente, i blocchi di tale componente diventano ora parte dell'ordine di blocco implicito, anche se non si dispone di visibilità in tali blocchi.

Ciò è ancora più difficile perché le operazioni di blocco includono molto più delle consuete funzioni per sezioni critiche, mutex e altri blocchi tradizionali. Tutte le chiamate di blocco che attraversano i limiti dei thread hanno proprietà di sincronizzazione che possono causare un deadlock. Il thread chiamante esegue un'operazione con la semantica ' Acquisisci ' e non può essere sbloccato fino a quando il thread di destinazione ' rilascia ' che chiama. Alcune funzioni User32 (ad esempio SendMessage), così come molte chiamate COM di blocco, rientrano in questa categoria.

Peggio ancora, il sistema operativo ha un blocco interno specifico del processo che talvolta viene mantenuto durante l'esecuzione del codice. Questo blocco viene acquisito quando le dll vengono caricate nel processo ed è quindi chiamato "blocco del caricatore". La funzione DllMain viene sempre eseguita sotto il blocco del caricatore; Se si acquisiscono blocchi in DllMain (e non è consigliabile), è necessario fare in modo che il caricatore blocchi la parte dell'ordine di blocco. La chiamata di determinate API Win32 potrebbe inoltre acquisire il blocco del caricatore per conto dell'utente, ad esempio LoadLibraryEx, GetModuleHandle e in particolare CoCreateInstance.

Per unire tutto questo insieme, esaminare il codice di esempio riportato di seguito. Questa funzione acquisisce più oggetti di sincronizzazione e definisce in modo implicito un ordine di blocco, un'operazione che non è necessariamente ovvia sull'ispezione del cursore. Sulla voce della funzione, il codice acquisisce una sezione critica e non la rilascia fino alla chiusura della funzione, rendendola quindi il nodo principale nella gerarchia dei blocchi. Il codice chiama quindi la funzione Win32 LoadIcon (), che dietro le quinte potrebbe chiamare il caricatore del sistema operativo per caricare il file binario. Questa operazione acquisisce il blocco del caricatore, che ora diventa anche parte di questa gerarchia di blocchi (assicurarsi che la funzione DllMain non acquisisca il \_ blocco g CS). Successivamente, il codice chiama SendMessage (), un'operazione cross-thread di blocco, che non verrà restituita a meno che il thread dell'interfaccia utente non risponda. Anche in questo caso, assicurarsi che il thread dell'interfaccia utente non acquisisca mai g \_ cs.

```
bool foo::bar (char* buffer)  
{  
      EnterCriticalSection(&g_cs);  
      // Get 'new data' icon  
      this.m_Icon = LoadIcon(hInst, MAKEINTRESOURCE(5));  
      // Let UI thread know to update icon SendMessage(hWnd,WM_COMMAND,IDM_ICON,NULL);  
      this.m_Params = GetParams(buffer);  
      LeaveCriticalSection(&g_cs);
      return true;  
}  
```

Esaminando questo codice è evidente che è stato creato in modo implicito g \_ cs come blocco di primo livello nella gerarchia dei blocchi, anche se si voleva solo sincronizzare l'accesso alle variabili membro della classe.

**Fare**

-   Progettare una gerarchia di blocchi e rispettarla. Aggiungere tutti i blocchi necessari. Sono disponibili molte più primitive di sincronizzazione rispetto a mutex e CriticalSections; tutti devono essere inclusi. Includere il blocco del caricatore nella gerarchia se si accettano blocchi in DllMain ()
-   Accetta il protocollo di blocco con le dipendenze. Qualsiasi codice chiamato dall'applicazione o che potrebbe chiamare l'applicazione deve condividere la stessa gerarchia di blocco
-   Bloccare le strutture dei dati non funzioni. Spostare le acquisizioni dei blocchi dai punti di ingresso della funzione e sorvegliare solo l'accesso ai dati con blocchi. Se un minor numero di codice opera sotto un blocco, è possibile che si verifichino deadlock
-   Analizzare le acquisizioni e i rilasci dei blocchi nel codice di gestione degli errori. Spesso la gerarchia di blocco viene dimenticata quando si tenta di eseguire il ripristino da una condizione di errore
-   Sostituire i blocchi annidati con i contatori di riferimento. Impossibile eseguire il deadlock. Gli elementi bloccati singolarmente negli elenchi e nelle tabelle sono candidati validi
-   Prestare attenzione quando si è in attesa di un handle di thread da una DLL. Si supponga sempre che il codice possa essere chiamato sotto il blocco del caricatore. È preferibile fare riferimento al conteggio delle risorse e lasciare che il thread di lavoro esegua la pulizia (e quindi usare FreeLibraryAndExitThread per terminare in modo corretto)
-   Usare l'API di attraversamento della catena di attesa se si vuole diagnosticare i deadlock

**Non:**

-   Eseguire operazioni diverse dall'inizializzazione molto semplice nella funzione DllMain (). Per ulteriori informazioni, vedere funzione di callback DllMain. In particolare, non chiamare LoadLibraryEx o CoCreateInstance
-   Scrivere le primitive di blocco personalizzate. Il codice di sincronizzazione personalizzato può introdurre con facilità bug sottili nella codebase. Usare invece la selezione avanzata degli oggetti di sincronizzazione del sistema operativo
-   Eseguire qualsiasi operazione nei costruttori e nei distruttori per le variabili globali che vengono eseguite sotto il blocco del caricatore

**Prestare attenzione con le eccezioni**

Le eccezioni consentono la separazione del normale flusso di programma e della gestione degli errori. A causa di questa separazione, può essere difficile individuare lo stato preciso del programma prima dell'eccezione e il gestore di eccezioni potrebbe perdere i passaggi cruciali per il ripristino di uno stato valido. Ciò è particolarmente vero per le acquisizioni di blocchi che devono essere rilasciate nel gestore per evitare deadlock futuri.

Il codice di esempio seguente illustra questo problema. L'accesso non associato alla variabile "buffer" provocherà occasionalmente una violazione di accesso (AV). Questo AV viene rilevato dal gestore di eccezioni native, ma non ha un modo semplice per determinare se la sezione critica è già stata acquisita al momento dell'eccezione (l'AV potrebbe essere stato preso in un punto qualsiasi del codice EnterCriticalSection).

```
 BOOL bar (char* buffer)  
{  
   BOOL rc = FALSE;  
   __try {  
      EnterCriticalSection(&cs);  
      while (*buffer++ != '&') ;  
      rc = GetParams(buffer);  
      LeaveCriticalSection(&cs);  
   } __except (EXCEPTION_EXECUTE_HANDLER)  
   {  
      return FALSE;  
   } 
   return rc;  
}  
```

**Fare**

-   Rimuovere \_ \_ try/ \_ \_ except quando possibile; non usare SetUnhandledExceptionFilter
-   Eseguire il wrapping dei blocchi in \_ modelli personalizzati di tipo PTR automatico se si usano le eccezioni C++. Il blocco deve essere rilasciato nel distruttore. Per le eccezioni native rilascia i blocchi nell' \_ \_ istruzione finally
-   Prestare attenzione al codice in esecuzione in un gestore di eccezioni native; è possibile che l'eccezione abbia perso molti blocchi, quindi il gestore non deve acquisire alcun

**Non:**

-   Gestire le eccezioni native se non sono necessarie o richieste dalle API Win32. Se si utilizzano gestori di eccezioni nativi per la creazione di report o il ripristino dei dati dopo errori irreversibili, provare a utilizzare il meccanismo del sistema operativo predefinito di Segnalazione errori Windows
-   Usare le eccezioni C++ con qualsiasi tipo di codice dell'interfaccia utente (User32); un'eccezione generata in un callback verrà spostata attraverso i livelli del codice C forniti dal sistema operativo. Il codice non è a conoscenza della semantica di unroll di C++

## <a name="links-to-resources"></a>Collegamenti alle risorse

-   [Segnalazione errori Windows](../wer/windows-error-reporting.md)
-   [Progettazione asincrona](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [I/O asincrono](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**AttachThreadInput (funzione)**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**\_classe PTR automatico**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**DisableProcessWindowsGhosting (funzione)**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**Funzione di callback DllMain**](../dlls/dllmain.md)
-   [Eventi](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**GetMessage (funzione)**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [Annullamento I/O](../fileio/canceling-pending-i-o-operations.md)
-   [**IsHungAppWindow (funzione)**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Coda messaggi](../winmsg/using-messages-and-message-queues.md)
-   [**MsgWaitForMultipleObjects (funzione)**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Nuova API del pool di thread](../procthread/thread-pool-api.md)
-   [**Funzione PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Riavvio e ripristino](../recovery/registering-for-application-restart.md)
-   [**SendMessageCallback (funzione)**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**SendNotifyMessage (funzione)**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Oggetti di sincronizzazione](../sync/about-synchronization.md)
-   [**TerminateThread (funzione)**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Segnalazione errori Windows](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
