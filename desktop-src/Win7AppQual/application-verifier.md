---
description: .
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946d27ecfef46766fe82cc4df2061c7fa5196a45
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314994"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows XP, Windows Vista, Windows 7  
**Server** : windows Server 2003, windows Server 2008, windows Server 2008 R2  


## <a name="description"></a>Descrizione

Promuovere e applicare Application Verifier come un controllo di qualità per tutto lo sviluppo. Sono inclusi diversi miglioramenti:

-   Sono stati forniti controlli aggiuntivi per risolvere i problemi rilevati dal team Segnalazione errori Windows durante l'utilizzo del pool di thread.
-   Sono state combinate le versioni a 32 e 64 bit del pacchetto per risolvere le modifiche apportate a Windows 7, incluse le esigenze per il test dei componenti a 32 bit in una versione a 64 bit di Windows, nonché per semplificare la norma.
-   Sono stati inclusi controlli aggiuntivi per le applicazioni multithreading, che eseguono applicazioni a 32 bit su Windows a 64 bit, oltre a numerose correzioni di bug.

Queste modifiche non dovrebbero avere alcun impatto negativo sugli utenti che non abilitano i controlli dei thread. coloro che ricevono supporto aggiuntivo per l'individuazione e la diagnosi dei problemi di utilizzo del pool di thread esistenti. Se si abilitano i controlli dei thread, si trarranno vantaggio dagli altri miglioramenti e correzioni di bug in questo servizio.

Sebbene si verifichi una lieve riduzione delle prestazioni quando si utilizza questo servizio, i livelli di prestazioni devono rimanere accettabili poiché in genere non vengono eseguiti in ambienti al dettaglio.

## <a name="usage"></a>Utilizzo

**Informazioni generali**

Per fornire applicazioni Windows affidabili:

1.  Testare le applicazioni scritte in codice non gestito (nativo) con Application Verifier nel debugger e con l'heap a pagina intera prima di rilasciarlo ai clienti.
2.  Seguire i passaggi forniti da Application Verifier per risolvere le condizioni errate.
3.  Una volta rilasciata l'applicazione, monitorare regolarmente i report sugli errori dell'applicazione raccolti da Segnalazione errori Windows.

I controlli dei pool di thread sono abilitati per impostazione predefinita sotto l'intestazione di controllo "Nozioni di base". Poiché è incluso nell'impostazione predefinita, gli utenti devono solo eseguire Application Verifier sul proprio codice con le impostazioni predefinite per sfruttare i nuovi controlli.

**Dettagli**

Come minimo, è necessario eseguire Application Verifier con l'impostazione di base selezionata. Questa operazione è necessaria per WinLogo e WinQual. L'impostazione di base verifica quanto segue:

-   **Dettagli arresto eccezioni** : garantisce che le applicazioni non nascondano violazioni di accesso mediante la gestione strutturata delle eccezioni
-   **Gestisce i dettagli di arresto** -test per assicurarsi che l'applicazione non tenti di usare handle non validi
-   **Dettagli arresto heap** : verifica la presenza di problemi di danneggiamento della memoria nell'heap
-   **Dettagli dell'interruzione di input/output** : esegue il monitoraggio dell'esecuzione di i/o asincrono ed esegue diverse convalide
-   **Dettagli interruzione della perdita** : rileva le perdite tenendo traccia delle risorse eseguite da una dll che non vengono liberate dal momento in cui la dll è stata scaricata
-   **Dettagli arresto blocchi** : verifica l'utilizzo corretto per le sezioni critiche
-   **Dettagli dell'arresto della memoria** : garantisce l'uso corretto delle API per le manipolazioni dello spazio virtuale (ad esempio, VirtualAlloc, MapViewOfFile)
-   **Dettagli stop TLS** : garantisce che le API di archiviazione locale di thread vengano usate correttamente
-   **Dettagli stop ThreadPool** : garantisce l'utilizzo corretto delle API ThreadPool e impone le verifiche di coerenza sugli stati thread di lavoro dopo un callback

Se l'applicazione esegue la migrazione da un'applicazione "precedente a vista", sarà necessario sfruttare i "LuaPriv" (noti anche come controlli UAC). Il predittore dei privilegi dell'account utente limitato (LuaPriv) ha due obiettivi principali:

-   **Predittiva**: durante l'esecuzione di un'applicazione con privilegi amministrativi, prevedere se l'applicazione funzionerà anche se eseguita con meno privilegi, in genere come utente normale. Se, ad esempio, l'applicazione scrive nei file che consentono l'accesso solo agli amministratori, l'applicazione non sarà in grado di scrivere nello stesso file se eseguita come non amministratore.
-   **Diagnostica**: durante l'esecuzione con privilegi non amministrativi, identificare i potenziali problemi che potrebbero già esistere con l'esecuzione corrente. Continuando l'esempio precedente, se l'applicazione tenta di scrivere in un file che concede l'accesso solo ai membri del gruppo Administrators, l'applicazione riceverà un errore di accesso \_ negato. Se l'applicazione non funziona correttamente, questa operazione potrebbe essere il colpevole.

LuaPriv identifica i tipi di problemi seguenti:



| **Potenziale problema**       | **Descrizione**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spazi dei nomi limitati     | La creazione di un oggetto di sincronizzazione denominato (evento, semaforo, mutex e così via) senza uno spazio dei nomi può complicare l'esecuzione senza privilegi in alcuni sistemi operativi, perché il sistema operativo può scegliere di collocare l'oggetto in uno spazio dei nomi con restrizioni. La creazione di un oggetto di questo tipo in uno spazio dei nomi con restrizioni, ad esempio lo spazio dei nomi globale, richiede SeCreateGlobalPrivilege, che viene concesso solo agli amministratori.<br/> LuaPriv contrassegna entrambi questi problemi se li rileva.<br/> |
| Controlli dell'amministratore hardware | Alcune applicazioni interrogano il token di sicurezza dell'utente per individuare la quantità di privilegi che possiede. In questi casi, l'applicazione può modificare il proprio comportamento in base alla quantità di energia ripensata dall'utente. <br/> LuaPriv contrassegna le chiamate API che restituiscono queste informazioni.<br/>                                                                                                                                                                                                |
| Richiesta di privilegi     | Un'applicazione può tentare di abilitare un privilegio pertinente per la sicurezza, ad esempio SeTcbPrivilege o SeSecurityPrivilege, prima di eseguire un'operazione che la richiede. <br/> I flag LuaPriv tentano di abilitare i privilegi relativi alla sicurezza. <br/>                                                                                                                                                                                                                               |
| Privilegi mancanti        | Se un'applicazione tenta di abilitare un privilegio di cui l'utente non dispone, probabilmente segnala che l'applicazione prevede il privilegio, che può causare differenze di comportamento. <br/> Richieste di privilegio non riuscite dei flag LuaPriv. <br/>                                                                                                                                                                                                                                       |
| Operazioni di INI-File       | I tentativi di scrittura nei file INI mappati (WritePrivateProfileSection e API simili) possono avere esito negativo come utente non amministratore. <br/> LuaPriv contrassegna tali operazioni.<br/>                                                                                                                                                                                                                                                                                                            |
| Accesso negato             | Se l'applicazione tenta di accedere a un oggetto (file, chiave del registro di sistema e così via), ma il tentativo ha esito negativo a causa di un accesso insufficiente, è probabile che l'applicazione sia in esecuzione con un numero maggiore di privilegi rispetto a. <br/> LuaPriv Flags-apre i tentativi che hanno esito negativo con accesso \_ negato ed errori simili.<br/>                                                                                                                                                               |
| Impedisci ACE                 | Se un oggetto dispone di voci ACE di negazione nell'elenco DACL, viene negato in modo esplicito l'accesso a entità specifiche. <br/> Si tratta di un'operazione non comune e rende difficile la stima, quindi i flag LuaPriv negano le voci ACE quando vengono trovati.<br/>                                                                                                                                                                                                                                                                     |
| Accesso limitato         | Se un'applicazione tenta di aprire un oggetto per i diritti non concessi agli utenti normali, ad esempio se si tenta di scrivere in un file che può essere scritto solo dagli amministratori, l'applicazione probabilmente non funzionerà nello stesso modo quando viene eseguita come utente normale. <br/> LuaPriv contrassegna tali operazioni.<br/>                                                                                                                                                                      |
| MASSIMO \_ consentito          | Se un'applicazione apre un oggetto per il massimo \_ consentito, il controllo di accesso effettivo sull'oggetto verrà eseguito altrove. La maggior parte del codice che esegue questa operazione non funziona correttamente e quasi certamente funziona in modo diverso quando viene eseguito senza privilegi. <br/> LuaPriv contrassegna quindi tutti gli eventi imprevisti di massimo \_ consentito. <br/>                                                                                                                                                            |



 

I problemi comunemente trascurati vengono acquisiti nei controlli varie nebulosi:

-   Dettagli arresto API pericolose
-   Dettagli arresto stack Dirty
-   Rollover ora

È stato aggiunto un nuovo verificatore di stampa. Questo livello consente di individuare e risolvere i problemi che possono verificarsi quando un'applicazione chiama il sottosistema di stampa. Print Verifier è destinato ai due livelli del sottosistema di stampa, al livello PrintAPI e al livello PrintDriver.

*Livello API di stampa*

Print Verifier Verifica l'interfaccia tra un programma e winspool. drv e prntvpt.dll e testa le interfacce di tali dll. È possibile esaminare le regole per chiamare le funzioni in questa interfaccia nella sezione della Guida di MSDN per le API esportate da winspool. drv e prntvpt.dll.

*Livello driver di stampa*

Il verificatore di stampa verifica inoltre l'interfaccia tra un driver di stampa di base, ad esempio UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL o MXDWDRV.DLL e i plug-in del driver di stampa. È possibile trovare informazioni su questa interfaccia in MSDN e in WDK.

Si noti che alcuni di questi controlli si riferiscono solo a Windows 7 e gli altri eseguono prestazioni migliori in Windows 7.

In genere, solo le versioni di debug eseguono il Application Verifier, quindi le prestazioni non sono in genere un problema. Se si verificano problemi di prestazioni dovuti all'uso di questo o di qualsiasi altro controllo Application Verifier, eseguire un controllo alla volta fino a quando non sono stati eseguiti tutti i controlli necessari.

Quasi il 10% degli arresti anomali dell'applicazione nei sistemi Windows sono dovuti a un danneggiamento dell'heap. È quasi impossibile eseguire il debug di questi arresti anomali dopo il fatto. Il modo migliore per evitare questi problemi consiste nel testare le funzionalità dell'heap di pagina disponibili in Application Verifier. Esistono due tipi di heap di pagina: "full" e "Light". Il valore predefinito è full. l'arresto del debugger verrà forzato immediatamente quando si rileva il danneggiamento. Questa funzionalità deve essere eseguita nel debugger. Tuttavia, è anche la maggior parte delle risorse richieste. Se un utente ha problemi di temporizzazione ed è già in esecuzione uno scenario in un heap di pagine "completo", è probabile che l'impostazione di questa opzione su "Light" affronti questi problemi. Inoltre, l'heap della pagina chiara non si arresta in modo anomalo fino alla chiusura del processo. Fornisce una traccia dello stack per l'allocazione, ma può richiedere molto più tempo per la diagnosi rispetto alla propria controparte completa.

Monitorare lo stato di affidabilità delle applicazioni tramite il portale Web di winqual. Questo portale Mostra i report degli errori raccolti tramite Segnalazione errori Windows, quindi è facile identificare gli errori più frequenti. Per informazioni, vedere Segnalazione errori Windows: Introduzione. Microsoft non addebita questo servizio.

Per sfruttare i vantaggi di WinQual, è necessario:

1.  Registrare la società per WinQual, che richiede un ID VeriSign. È possibile trovare informazioni su WinQual nel portale per sviluppatori raggruppate in Windows Vista SP1 \\ Windows Server 2008. Il percorso di Windows 7 sarà presto disponibile.
2.  Eseguire il mapping delle applicazioni ISV a un nome di prodotto e al nome ISV, che collega i report sugli errori alla società. Gli altri ISV non possono visualizzare i report degli errori.
3.  Usare il portale per identificare i problemi principali. Gli ISV possono inoltre creare risposte per informare i clienti di quali passaggi eseguire in seguito a un errore. Il sistema di risposta supporta oltre 10 lingue in tutto il mondo.

Si noti inoltre che Application Verifier è altrettanto efficace dei percorsi di codice in cui viene eseguito. Il valore di combinazione di questo strumento con uno strumento di code coverage non può essere sovrastato.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

**Strumenti di debug per Windows:**

-   [Panoramica e sito di download](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [Documentazione online di MSDN](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Overview](/previous-versions/ms220948(v=vs.80))
-   [Scaricare](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier per Microsoft Visual Studio 2008/.NET Framework 3,5](/previous-versions/ms220948(v=vs.80))

    **Nota:** la versione di Application Verifier fornita in Visual Studio è piuttosto data. Se possibile, usare invece il pacchetto autonomo. Per questo motivo, le versioni future di Visual Studio non saranno più incorporate Application Verifier.

**WinQual**

-   [Servizi online di qualità Windows (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Segnalazione errori Windows: Introduzione](../wer/using-wer.md)

 

 
