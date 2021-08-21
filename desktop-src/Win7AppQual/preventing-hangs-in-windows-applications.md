---
description: Informazioni su come evitare blocchi nelle applicazioni Windows per Windows 7 e Windows server 2008 R2.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Prevenzione dei blocchi nelle Windows applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5509b8733e45b105694a8bfdadddae0d67096b92c390ed98b3dd937817823b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994826"
---
# <a name="preventing-hangs-in-windows-applications"></a>Prevenzione dei blocchi nelle Windows applicazioni

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="description"></a>Descrizione

**Blocchi - Prospettiva dell'utente**

Agli utenti piacciono le applicazioni reattive. Quando fanno clic su un menu, vogliono che l'applicazione reagisca immediatamente, anche se sta stampando il proprio lavoro. Quando salvano un documento lungo nel word processor preferito, vogliono continuare a digitare mentre il disco è ancora in rotazione. Gli utenti si insoddisfaceno piuttosto rapidamente quando l'applicazione non reagisce in modo rapido all'input.

Un programmatore potrebbe riconoscere molti motivi legittimi per cui un'applicazione non risponde immediatamente all'input dell'utente. L'applicazione potrebbe essere occupata a ricalcolare alcuni dati o semplicemente in attesa del completamento dell'I/O su disco. Tuttavia, dalla ricerca degli utenti, si sa che gli utenti sono infastiditi e frustrati dopo solo un paio di secondi di insensibilità. Dopo 5 secondi, tenteranno di terminare un'applicazione bloccata. Accanto agli arresti anomali, i blocchi dell'applicazione sono l'origine più comune di interruzioni dell'utente quando si lavora con le applicazioni Win32.

Esistono molte cause radice diverse per il blocco dell'applicazione e non tutte si manifestano in un'interfaccia utente che non risponde. Tuttavia, un'interfaccia utente che non risponde è una delle esperienze di blocco più comuni e questo scenario attualmente riceve il maggior supporto del sistema operativo sia per il rilevamento che per il ripristino. Windows rileva automaticamente, raccoglie informazioni di debug e facoltativamente termina o riavvia le applicazioni in sospeso. In caso contrario, l'utente potrebbe dover riavviare il computer per ripristinare un'applicazione bloccata.

**Blocchi - Prospettiva del sistema operativo**

Quando un'applicazione (o più precisamente un thread) crea una finestra sul desktop, immette un contratto implicito con il Gestione finestre desktop (DWM) per elaborare i messaggi della finestra in modo temporale. DWM invia messaggi (input da tastiera/mouse e messaggi da altre finestre, nonché da se stesso) nella coda di messaggi specifica del thread. Il thread recupera e invia tali messaggi tramite la relativa coda di messaggi. Se il thread non esegue il servizio della coda chiamando GetMessage(), i messaggi non vengono elaborati e la finestra si blocca: non può né ridisegnare né accettare l'input dell'utente. Il sistema operativo rileva questo stato allegando un timer ai messaggi in sospeso nella coda di messaggi. Se un messaggio non è stato recuperato entro 5 secondi, DWM dichiara che la finestra deve essere bloccata. È possibile eseguire query su questo particolare stato della finestra tramite l'API IsHungAppWindow().

Il rilevamento è solo il primo passaggio. A questo punto, l'utente non può ancora terminare l'applicazione. Facendo clic sul pulsante X (Chiudi) viene visualizzato un messaggio WM CLOSE, che rimane bloccato nella coda di messaggi come qualsiasi \_ altro messaggio. Il Gestione finestre desktop assiste nascondendo e quindi sostituendo la finestra bloccata con una copia "fantasma" che visualizza una bitmap dell'area client precedente della finestra originale (e aggiungendo "Non risponde" alla barra del titolo). Purché il thread della finestra originale non recuperi i messaggi, DWM gestisce entrambe le finestre contemporaneamente, ma consente all'utente di interagire solo con la copia fantasma. Usando questa finestra fantasma, l'utente può solo spostare, ridurre a icona e, soprattutto, chiudere l'applicazione che non risponde, ma non modificarne lo stato interno.

L'intera esperienza fantasma è simile alla seguente:

![Screenshot che mostra la finestra di dialogo "Blocco note non risponde".](images/preventinghangs-ghostwindow.gif)

Il Gestione finestre desktop esegue un'ultima cosa; si integra con Segnalazione errori Windows, consentendo all'utente non solo di chiudere e facoltativamente riavviare l'applicazione, ma anche di inviare dati di debug importanti a Microsoft. È possibile ottenere questi dati di blocco per le proprie applicazioni registrarsi nel sito Web Winqual.

Windows 7 ha aggiunto una nuova funzionalità a questa esperienza. Il sistema operativo analizza l'applicazione bloccata e, in determinate circostanze, offre all'utente la possibilità di annullare un'operazione di blocco e rendere nuovamente reattiva l'applicazione. L'implementazione corrente supporta l'annullamento delle chiamate Socket bloccanti. Altre operazioni saranno annullabili dall'utente nelle versioni future.

Per integrare l'applicazione con l'esperienza di ripristino del blocco e per ottenere il massimo dei dati disponibili, seguire questa procedura:

-   Assicurarsi che l'applicazione si registri per il riavvio e il ripristino, rendendo un blocco il più possibile indolore per l'utente. Un'applicazione registrata correttamente può essere riavviata automaticamente con la maggior parte dei dati non salvati intatta. Questa operazione funziona sia per blocchi che arresti anomali dell'applicazione.
-   Ottenere informazioni sulla frequenza e sul debug dei dati per le applicazioni bloccate e bloccate dal sito Web Winqual. È possibile usare queste informazioni anche durante la versione Beta per migliorare il codice. Vedere "Introduzione Segnalazione errori Windows" per una breve panoramica.
-   È possibile disabilitare la funzionalità di ghosting nell'applicazione tramite una chiamata a DisableProcessWindowsGhosting (). Ciò impedisce tuttavia all'utente medio di chiudere e riavviare un'applicazione bloccata e spesso termina con un riavvio.

**Blocchi - Prospettiva per gli sviluppatori**

Il sistema operativo definisce un blocco dell'applicazione come thread dell'interfaccia utente che non ha elaborato messaggi per almeno 5 secondi. Bug evidenti causano alcuni blocchi, ad esempio un thread in attesa di un evento che non viene mai segnalato e due thread ognuno con un blocco e tentando di acquisire gli altri. È possibile correggere questi bug senza troppi sforzi. Tuttavia, molti blocchi non sono così chiari. Sì, il thread dell'interfaccia utente non sta recuperando messaggi, ma è ugualmente occupato a eseguire altre operazioni "importanti" e alla fine tornerà all'elaborazione dei messaggi.

Tuttavia, l'utente lo considera un bug. La progettazione deve corrispondere alle aspettative dell'utente. Se la progettazione dell'applicazione porta a un'applicazione che non risponde, la progettazione dovrà cambiare. Infine, ed è importante, non è possibile rispondere come un bug del codice. richiede operazioni iniziali durante la fase di progettazione. Il tentativo di modificare la base di codice esistente di un'applicazione per rendere l'interfaccia utente più reattiva è spesso troppo costoso. Le linee guida di progettazione seguenti possono essere utili.

-   Rendere la velocità di risposta dell'interfaccia utente un requisito di primo livello; l'utente deve sempre avere il controllo dell'applicazione
-   Assicurarsi che gli utenti possano annullare le operazioni che richiede più di un secondo per il completamento e/o che le operazioni possano essere completate in background. fornire l'interfaccia utente di stato appropriata, se necessario

![Screenshot che mostra la finestra di dialogo "Copia di elementi".](images/preventinghangs-progressbar.gif)

-   Accodare operazioni a esecuzione lunga o di blocco come attività in background (questo richiede un meccanismo di messaggistica ben pensato per informare il thread dell'interfaccia utente quando il lavoro è stato completato)
-   Mantenere il codice per i thread dell'interfaccia utente semplice; rimuovere il maggior numero possibile di chiamate API bloccante
-   Mostra finestre e finestre di dialogo solo quando sono pronte e completamente operative. Se la finestra di dialogo deve visualizzare informazioni che richiedono un utilizzo elevato di risorse per il calcolo, visualizzare prima alcune informazioni generiche e aggiornarlo in tempo reale quando saranno disponibili più dati. Un buon esempio è la finestra di dialogo delle proprietà della cartella Windows Explorer. Deve visualizzare le dimensioni totali della cartella, le informazioni che non sono immediatamente disponibili dal file system. La finestra di dialogo viene visualizzata immediatamente e il campo "size" viene aggiornato da un thread di lavoro:

![Screenshot che mostra la pagina "Generale" Windows proprietà con il testo "Size", "Size on disk" e "Contains" cerchiato.](images/preventinghangs-updatingdialog.gif)

Sfortunatamente, non esiste un modo semplice per progettare e scrivere un'applicazione reattiva. Windows non fornisce un framework asincrono semplice che consenta una pianificazione semplice delle operazioni di blocco o a esecuzione lunga. Le sezioni seguenti illustrano alcune delle procedure consigliate per evitare blocchi ed evidenziano alcune delle insidie comuni.

## <a name="best-practices"></a>Procedure consigliate

**Mantenere il thread dell'interfaccia utente semplice**

La responsabilità principale del thread dell'interfaccia utente è recuperare e inviare messaggi. Qualsiasi altro tipo di lavoro introduce il rischio di sospensione delle finestre di proprietà di questo thread.

**fare:**

-   Spostare algoritmi a elevato utilizzo di risorse o non associati che comportano operazioni a esecuzione lunga nei thread di lavoro
-   Identificare il maggior numero possibile di chiamate di funzione di blocco e provare a spostarle nei thread di lavoro. qualsiasi funzione che chiama in un'altra DLL deve essere sospetta
-   È possibile rimuovere tutte le chiamate api di rete e I/O di file dal thread di lavoro. Queste funzioni possono bloccarsi per molti secondi, se non minuti. Se è necessario eseguire qualsiasi tipo di I/O nel thread dell'interfaccia utente, è consigliabile usare l'I/O asincrono
-   Tenere presente che il thread dell'interfaccia utente esegue anche la manutenzione di tutti i server COM apartment a thread singolo ospitati dal processo. se si effettua una chiamata di blocco, questi server COM non rispondono fino a quando non si rispetti la coda di messaggi

**Non:**

-   Attendere un oggetto kernel (ad esempio Event o Mutex) per più di un periodo di tempo molto breve; se è necessario attendere, provare a usare MsgWaitForMultipleObjects(), che si sbloccherà all'arrivo di un nuovo messaggio
-   Condividere la coda di messaggi della finestra di un thread con un altro thread usando la funzione AttachThreadInput(). Non solo è estremamente difficile sincronizzare correttamente l'accesso alla coda, ma può anche impedire al sistema operativo Windows di rilevare correttamente una finestra bloccata
-   Usare TerminateThread() in uno dei thread di lavoro. La terminazione di un thread in questo modo non consente di rilasciare blocchi o segnali eventi e può causare facilmente oggetti di sincronizzazione orfani
-   Chiamare qualsiasi codice "sconosciuto" dal thread dell'interfaccia utente. Ciò vale soprattutto se l'applicazione ha un modello di estendibilità. non è garantito che il codice di terze parti segua le linee guida sulla velocità di risposta
-   Effettuare qualsiasi tipo di chiamata broadcast di blocco; SendMessage(HWND BROADCAST) si trova alla mercé di \_ ogni applicazione non scritta attualmente in esecuzione

**Implementare modelli asincroni**

La rimozione di operazioni a esecuzione lunga o di blocco dal thread dell'interfaccia utente richiede l'implementazione di un framework asincrono che consenta l'offload di tali operazioni ai thread di lavoro.

**fare:**

-   Usare le API dei messaggi di finestra asincrone nel thread dell'interfaccia utente, in particolare sostituendo SendMessage con uno dei peer non bloccanti: PostMessage, SendNotifyMessage o SendMessageCallback
-   Usare i thread in background per eseguire attività a esecuzione lunga o di blocco. Usare la nuova API del pool di thread per implementare i thread di lavoro
-   Fornire il supporto dell'annullamento per le attività in background a esecuzione lunga. Per bloccare le operazioni di I/O, usare l'annullamento di I/O, ma solo come ultima risorsa. non è facile annullare l'operazione 'right'
-   Implementare una progettazione asincrona per il codice gestito usando il modello IAsyncResult o gli eventi

**Usare i blocchi in modo oculato**

L'applicazione o la DLL richiede blocchi per sincronizzare l'accesso alle strutture di dati interne. L'uso di più blocchi aumenta il parallelismo e rende l'applicazione più reattiva. Tuttavia, l'uso di più blocchi aumenta anche la probabilità di acquisire tali blocchi in ordini diversi e causando il deadlock dei thread. Se due thread contengono un blocco e quindi tentano di acquisire il blocco dell'altro thread, le operazioni formeranno un'attesa circolare che blocca lo stato di avanzamento per questi thread. È possibile evitare questo deadlock solo assicurando che tutti i thread nell'applicazione acquisiscono sempre tutti i blocchi nello stesso ordine. Tuttavia, non è sempre facile acquisire blocchi nell'ordine "corretto". I componenti software possono essere composti, ma non le acquisizioni di blocchi. Se il codice chiama un altro componente, i blocchi del componente diventano ora parte dell'ordine di blocco implicito, anche se non si ha visibilità su tali blocchi.

Le cose si complicano ancora perché le operazioni di blocco includono molto più delle normali funzioni per sezioni critiche, mutex e altri blocchi tradizionali. Qualsiasi chiamata di blocco che attraversa i limiti dei thread ha proprietà di sincronizzazione che possono causare un deadlock. Il thread chiamante esegue un'operazione con semantica 'acquire' e non può sbloccarsi fino a quando il thread di destinazione non rilascia la chiamata. In questa categoria rientrano alcune funzioni User32 ,ad esempio SendMessage, e molte chiamate COM bloccate.

Ancora peggiore, il sistema operativo ha un proprio blocco interno specifico del processo che talvolta viene mantenuto durante l'esecuzione del codice. Questo blocco viene acquisito quando le DLL vengono caricate nel processo e viene quindi chiamato "blocco del caricatore". La funzione DllMain viene sempre eseguita sotto il blocco del caricatore. se si acquisiscono blocchi in DllMain (e non è consigliabile), è necessario rendere il blocco del caricatore parte dell'ordine di blocco. La chiamata di determinate API Win32 potrebbe anche acquisire il blocco del caricatore per conto dell'utente, ad esempio funzioni come LoadLibraryEx, GetModuleHandle e in particolare CoCreateInstance.

Per associare tutto questo, esaminare il codice di esempio seguente. Questa funzione acquisisce più oggetti di sincronizzazione e definisce in modo implicito un ordine di blocco, qualcosa che non è necessariamente ovvio in caso di ispezione cursore. All'immissione della funzione, il codice acquisisce una sezione critica e non la rilascia fino all'uscita della funzione, rendendola quindi il nodo principale nella gerarchia di blocco. Il codice chiama quindi la funzione Win32 LoadIcon(), che potrebbe chiamare nel caricatore del sistema operativo per caricare questo file binario. Questa operazione acquisisce il blocco del caricatore, che ora diventa anche parte di questa gerarchia di blocchi (assicurarsi che la funzione DllMain non acquisisca il blocco g \_ cs). Il codice chiama quindi SendMessage(), un'operazione cross-thread di blocco, che non restituirà a meno che il thread dell'interfaccia utente non risponda. Anche in questo caso, assicurarsi che il thread dell'interfaccia utente non acquisisca mai g \_ cs.

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

Esaminando questo codice sembra chiaro che g cs sia stato implicitamente il blocco di primo livello nella gerarchia dei blocchi, anche se si vuole solo sincronizzare l'accesso alle variabili \_ membro della classe.

**fare:**

-   Progettare una gerarchia di blocchi e rispettarla. Aggiungere tutti i blocchi necessari. Sono disponibili molte più primitive di sincronizzazione rispetto solo a Mutex e CriticalSections. devono essere tutti inclusi. Includere il blocco del caricatore nella gerarchia se si accettano blocchi in DllMain()
-   Accettare il protocollo di blocco con le dipendenze. Qualsiasi codice chiamato dall'applicazione o che potrebbe chiamare l'applicazione deve condividere la stessa gerarchia di blocchi
-   Blocca le strutture dei dati non funziona. Spostare le acquisizioni di blocchi dai punti di ingresso della funzione e proteggere solo l'accesso ai dati con blocchi. Se meno codice opera sotto un blocco, è meno probabile che si siano verificati deadlock
-   Analizzare le acquisizioni e le versioni dei blocchi nel codice di gestione degli errori. Spesso la gerarchia di blocco viene dimenticata quando si tenta di eseguire il ripristino da una condizione di errore
-   Sostituire i blocchi annidati con i contatori di riferimento, che non possono essere deadlock. Gli elementi bloccati singolarmente in elenchi e tabelle sono buoni candidati
-   Prestare attenzione quando si attende un handle di thread da una DLL. Si supponga sempre che il codice possa essere chiamato sotto il blocco del caricatore. È meglio fare riferimento al conteggio delle risorse e consentire al thread di lavoro di eseguire la pulizia (e quindi usare FreeLibraryAndExitThread per terminare in modo pulito)
-   Usare l'API Wait Chain Traversal per diagnosticare i deadlock

**Non:**

-   Eseguire operazioni diverse dall'inizializzazione molto semplice nella funzione DllMain(). Per altri dettagli, vedere Funzione di callback DllMain. In particolare, non chiamare LoadLibraryEx o CoCreateInstance
-   Scrivere primitive di blocco. Il codice di sincronizzazione personalizzato può introdurre facilmente bug sottili nella codebase. Usare invece la selezione completa di oggetti di sincronizzazione del sistema operativo
-   Eseguire qualsiasi operazione nei costruttori e nei distruttori per le variabili globali, che vengono eseguite sotto il blocco del caricatore

**Prestare attenzione alle eccezioni**

Le eccezioni consentono la separazione del normale flusso del programma e della gestione degli errori. A causa di questa separazione, può essere difficile conoscere lo stato preciso del programma prima dell'eccezione e il gestore delle eccezioni potrebbe non eseguire passaggi cruciali per il ripristino di uno stato valido. Ciò vale soprattutto per le acquisizioni di blocchi che devono essere rilasciate nel gestore per evitare deadlock futuri.

Il codice di esempio seguente illustra questo problema. L'accesso non associato alla variabile "buffer" causa occasionalmente una violazione di accesso . Questo av viene intercettato dal gestore eccezioni nativo, ma non ha un modo semplice per determinare se la sezione critica è già stata acquisita al momento dell'eccezione (l'av potrebbe anche aver avuto luogo da qualche parte nel codice EnterCriticalSection).

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

**fare:**

-   Rimuovere \_ \_ try/ \_ \_ tranne quando possibile; non usare SetUnhandledExceptionFilter
-   Eseguire il wrapping dei blocchi in modelli personalizzati simili \_ a ptr se si usano eccezioni C++. Il blocco deve essere rilasciato nel distruttore. Per le eccezioni native rilasciare i blocchi \_ \_ nell'istruzione finally
-   Prestare attenzione con il codice in esecuzione in un gestore eccezioni nativo. l'eccezione potrebbe avere avuto molti blocchi, quindi il gestore non deve acquisire alcun

**Non:**

-   Gestire le eccezioni native se non sono necessarie o richieste dalle API Win32. Se si usano gestori eccezioni nativi per la creazione di report o il ripristino dei dati dopo errori irreversici, è consigliabile usare invece il meccanismo predefinito del sistema operativo Segnalazione errori Windows
-   Usare eccezioni C++ con qualsiasi tipo di codice dell'interfaccia utente (user32). un'eccezione generata in un callback attraversa i livelli di codice C forniti dal sistema operativo. Questo codice non conosce la semantica di annullamento della registrazione in C++

## <a name="links-to-resources"></a>Collegamenti alle risorse

-   [Segnalazione errori Windows](../wer/windows-error-reporting.md)
-   [Progettazione asincrona](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [I/O asincrono](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**Funzione AttachThreadInput**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**Classe \_ auto ptr**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**Funzione DisableProcessWindowsGhosting**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**Funzione di callback DllMain**](../dlls/dllmain.md)
-   [Eventi](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**Funzione GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [Annullamento di I/O](../fileio/canceling-pending-i-o-operations.md)
-   [**Funzione IsHungAppWindow**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [Coda messaggi](../winmsg/using-messages-and-message-queues.md)
-   [**Funzione MsgWaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Nuova API pool di thread](../procthread/thread-pool-api.md)
-   [**Funzione PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Riavvio e ripristino](../recovery/registering-for-application-restart.md)
-   [**Funzione SendMessageCallback**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**Funzione SendNotifyMessage**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Oggetti di sincronizzazione](../sync/about-synchronization.md)
-   [**Funzione TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Segnalazione errori Windows](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
