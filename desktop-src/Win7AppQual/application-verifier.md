---
description: Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac2a8bc900ea9d1f35ae228371226355657b930
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088689"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Promuovere e applicare la Application Verifier come controllo di qualità per tutto lo sviluppo. Include diversi miglioramenti:

-   Sono stati forniti controlli aggiuntivi per risolvere i problemi individuati dal team Segnalazione errori Windows durante l'utilizzo del pool di thread.
-   Sono state combinate le versioni a 32 e a 64 bit del pacchetto per risolvere le modifiche in Windows 7, incluse le esigenze di test dei componenti a 32 bit in una versione a 64 bit di Windows, nonché per la semplificazione generale.
-   Sono stati inclusi controlli aggiuntivi per le applicazioni multithreading, l'esecuzione di applicazioni a 32 bit in Windows a 64 bit, nonché molte correzioni di bug.

Queste modifiche non devono avere alcun impatto negativo sugli utenti che non abilitano i controlli dei thread. Gli utenti che lo fanno devono ricevere supporto aggiuntivo per l'individuazione e la diagnosi dei problemi di utilizzo del pool di thread esistenti. Indipendentemente dal fatto che si abilitino o meno i controlli dei thread, puoi trarre vantaggio dagli altri miglioramenti e correzioni di bug in questo servizio.

Anche se si verifica una lieve riduzione delle prestazioni quando si usa questo servizio, i livelli di prestazioni devono rimanere accettabili perché in genere non vengono eseguiti in ambienti di vendita al dettaglio.

## <a name="usage"></a>Utilizzo

**Informazioni generali**

Per distribuire applicazioni Windows affidabili:

1.  Testare le applicazioni scritte in codice non gestito (nativo) con Application Verifier nel debugger e con heap a pagina intera prima di rilasciarla ai clienti.
2.  Seguire i passaggi forniti da Application Verifier per risolvere le condizioni di errore.
3.  Dopo il rilascio dell'applicazione, monitorare regolarmente i report degli errori dell'applicazione raccolti da Segnalazione errori Windows.

I controlli del pool di thread sono abilitati per impostazione predefinita sotto l'intestazione di controllo "Informazioni di base". Poiché questa opzione è inclusa nell'impostazione predefinita, gli utenti devono solo eseguire Application Verifier sul codice con le impostazioni predefinite per sfruttare i nuovi controlli.

**Dettagli**

Come minimo, è necessario eseguire il Application Verifier con l'impostazione Informazioni di base selezionata. Questa operazione è necessaria per WinLogo e WinQual. L'impostazione Informazioni di base verifica quanto segue:

-   **Dettagli di arresto delle eccezioni:** garantisce che le applicazioni non nascondino le violazioni di accesso tramite la gestione delle eccezioni strutturata
-   **Gestisce i dettagli di arresto:** test per verificare che l'applicazione non tenti di usare handle non validi
-   **Dettagli sull'arresto degli** heap: verifica la presenza di problemi di danneggiamento della memoria nell'heap
-   **Dettagli arresto input/output:** monitora l'esecuzione di operazioni di I/O asincrone ed esegue varie convalide
-   **Dettagli arresto perdita:** rileva le perdite rilevando le risorse effettuate da una DLL che non vengono liberate al momento dello scaricamento della DLL
-   **Dettagli di arresto blocchi:** verifica l'utilizzo corretto per le sezioni critiche
-   **Dettagli sull'arresto** della memoria: garantisce che le API per le modifiche dello spazio virtuale vengano usate correttamente, ad esempio VirtualAlloc, MapViewOfFile
-   **Dettagli di arresto TLS:** garantisce che le API di archiviazione locale dei thread vengano usate correttamente
-   **Dettagli di arresto del** pool di thread: garantisce l'utilizzo corretto delle API del pool di thread e applica i controlli di coerenza sugli stati del thread di lavoro dopo un callback

Se l'applicazione esegue la migrazione da un'applicazione "Pre-Vista", è necessario sfruttare "LuaPriv" (noto anche come controllo dell'account utente). LuaPriv (Limited User Account Privilege Predictor) ha due obiettivi principali:

-   **Predittiva:** durante l'esecuzione di un'applicazione con privilegi amministrativi, stimare se tale applicazione funzionerà anche se eseguita con meno privilegi (in genere, come utente normale). Ad esempio, se l'applicazione scrive in file che consentono l'accesso solo agli amministratori, tale applicazione non sarà in grado di scrivere nello stesso file se eseguita come non amministratore.
-   **Diagnostica:** durante l'esecuzione con privilegi non di amministratore, identificare i potenziali problemi che potrebbero esistere già con l'esecuzione corrente. Continuando con l'esempio precedente, se l'applicazione tenta di scrivere in un file che concede l'accesso solo ai membri del gruppo Administrator, l'applicazione riceverà un errore di accesso \_ negato. Se l'applicazione non funziona correttamente, questa operazione potrebbe essere il responsabile.

LuaPriv identifica i tipi di problemi seguenti:



| **Potenziale problema**       | **Descrizione**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spazi dei nomi con restrizioni     | La creazione di un oggetto di sincronizzazione denominato (Evento, Semaforo, Mutex e così via) senza uno spazio dei nomi può complicare l'esecuzione senza privilegi in alcuni sistemi operativi perché il sistema operativo può scegliere di inserire l'oggetto in uno spazio dei nomi con restrizioni. Per creare un oggetto di questo tipo in uno spazio dei nomi con restrizioni, ad esempio lo spazio dei nomi Globale, è necessario seCreateGlobalPrivilege, che viene concesso solo agli amministratori.<br/> LuaPriv contrassegna entrambi questi problemi se vengono rilevati.<br/> |
| Verifiche dell'amministratore rigido | Alcune applicazioni interrogano il token di sicurezza dell'utente per scoprire quanti privilegi ha. In questi casi, l'applicazione può modificarne il comportamento a seconda della potenza che l'utente pensa di avere. <br/> LuaPriv contrassegna le chiamate API che restituiscono queste informazioni.<br/>                                                                                                                                                                                                |
| Richiesta di privilegi     | Un'applicazione può tentare di abilitare un privilegio pertinente alla sicurezza (ad esempio SeTcbPrivilege o SeSecurityPrivilege) prima di eseguire un'operazione che lo richiede. <br/> I flag LuaPriv tentano di abilitare i privilegi pertinenti alla sicurezza. <br/>                                                                                                                                                                                                                               |
| Privilegi mancanti        | Se un'applicazione tenta di abilitare un privilegio che l'utente non ha, è probabile che segnali che l'applicazione prevede il privilegio, che può causare differenze di comportamento. <br/> LuaPriv contrassegna le richieste di privilegi non riuscite. <br/>                                                                                                                                                                                                                                       |
| INI-File operazioni       | I tentativi di scrittura in file INI mappati (WritePrivateProfileSection e API simili) possono avere esito negativo come utente non amministratore. <br/> LuaPriv contrassegna tali operazioni.<br/>                                                                                                                                                                                                                                                                                                            |
| Accesso negato             | Se l'applicazione tenta di accedere a un oggetto (file, chiave del Registro di sistema e così via), ma il tentativo non riesce a causa di un accesso insufficiente, è probabile che l'applicazione sia in esecuzione con privilegi più elevati di quelli disponibili. <br/> LuaPriv contrassegna i tentativi di apertura di oggetti che hanno esito negativo con ACCESS \_ DENIED e errori simili.<br/>                                                                                                                                                               |
| Nega ACE                 | Se un oggetto dispone di ACE Deny nel relativo DACL, nega in modo esplicito l'accesso a entità specifiche. <br/> Questo non è insolito e rende difficile la stima, quindi LuaPriv contrassegna le voci ACE di negazione quando le trova.<br/>                                                                                                                                                                                                                                                                     |
| Accesso con restrizioni         | Se un'applicazione tenta di aprire un oggetto per i diritti non concessi agli utenti normali (ad esempio, il tentativo di scrivere in un file che può essere scritto solo dagli amministratori), è probabile che l'applicazione non funzionerà allo stesso modo quando viene eseguita come utente normale. <br/> LuaPriv contrassegna tali operazioni.<br/>                                                                                                                                                                      |
| MAXIMUM \_ ALLOWED          | Se un'applicazione apre un oggetto per MAXIMUM ALLOWED, il controllo di accesso \_ effettivo sull'oggetto verrà eseguito altrove. La maggior parte del codice che esegue questa operazione non funziona correttamente e quasi certamente funziona in modo diverso quando viene eseguito senza privilegi. <br/> LuaPriv contrassegna quindi tutti gli eventi imprevisti di MAXIMUM \_ ALLOWED. <br/>                                                                                                                                                            |



 

I problemi comunemente trascurati vengono acquisiti nelle verifiche varie nebulose:

-   Dettagli di arresto delle API pericolose
-   Dettagli di arresto degli stack dirty
-   Rollover temporale

È stato aggiunto un nuovo print verifier. Questo livello consente di individuare e risolvere i problemi che possono verificarsi quando un'applicazione chiama il sottosistema di stampa. Print Verifier è destinato ai due livelli del sottosistema di stampa, il livello PrintAPI e il livello PrintDriver.

*Livello API di stampa*

Print Verifier testa l'interfaccia tra un programma e Winspool.drv e prntvpt.dll le interfacce di tali DLL. È possibile esaminare le regole per chiamare le funzioni in questa interfaccia nella sezione della Guida MSDN per le API esportate da winspool.drv e prntvpt.dll.

*Livello driver di stampa*

Print Verifier verifica anche l'interfaccia tra un driver di stampa principale, ad esempio UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL o MXDWDRV.DLL e i plug-in del driver di stampa. Per informazioni su questa interfaccia, vedere MSDN e WDK.

Si noti che alcuni di questi controlli sono solo per Windows 7 e altri semplicemente migliorano le prestazioni in Windows 7.

In genere, solo le versioni di debug eseguono Application Verifier, quindi le prestazioni non sono in genere un problema. Se si verificano problemi di prestazioni derivanti dall'uso di questo o di qualsiasi altro controllo Application Verifier, eseguire un controllo alla volta fino a quando non sono stati eseguiti tutti i controlli necessari.

Quasi il 10% degli arresti anomali delle applicazioni nei sistemi Windows è dovuto al danneggiamento dell'heap. Questi arresti anomali sono quasi impossibili da eseguire dopo il fatto. Il modo migliore per evitare questi problemi è testare con le funzionalità dell'heap di pagina disponibili in Application Verifier. Esistono due tipi di heap di pagina: "Full" e "Light". Full è l'impostazione predefinita. forza l'arresto immediato di un debugger al rilevamento del danneggiamento. Questa funzionalità DEVE essere eseguita nel debugger. Tuttavia, è anche la risorsa più impegnativa. Se un utente presenta problemi di temporizzazione ed è già stato eseguito uno scenario nell'heap di pagine "Full", impostandolo su "Light" probabilmente questi problemi verranno risolti. Inoltre, l'heap di pagine leggere non si arresta in modo anomalo fino alla chiusura del processo. Fornisce un'analisi dello stack per l'allocazione, ma la diagnosi può richiedere molto più tempo rispetto all'uso della controparte Full.

Monitorare lo stato di affidabilità delle applicazioni tramite il portale Web Winqual. Questo portale mostra le segnalazioni degli errori raccolte tramite Segnalazione errori Windows, quindi è facile identificare gli errori più frequenti. Per altre informazioni, vedere Segnalazione errori Windows: Attività iniziali. Microsoft non addebita l'addebito per questo servizio.

Per sfruttare i vantaggi di WinQual, è necessario:

1.  Registrare la società per WinQual, che richiede un ID VeriSign. Le informazioni di Windows 7 su WinQual sono disponibili nel portale per sviluppatori raggruppate in Windows Vista SP1 \\ Windows Server 2008. A breve avrà una posizione di Windows 7.
2.  Eseguire il mapping delle applicazioni ISV a un nome di prodotto e al nome ISV, che collega i report degli errori alla società. Gli altri ISV non possono visualizzare le segnalazioni errori.
3.  Usare il portale per identificare i problemi principali. Gli ISV possono anche creare risposte che informano i clienti sui passaggi da eseguire dopo un errore. Il sistema di risposta supporta più di 10 lingue in tutto il mondo.

Un'altra nota: Application Verifier è valido solo come i percorsi di codice in cui viene eseguito. Il valore della combinazione di questo strumento con code coverage non può essere sovrascritto.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

**Strumenti di debug per Windows:**

-   [Panoramica e sito di download](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [Documentazione online MSDN](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Panoramica](/previous-versions/ms220948(v=vs.80))
-   [Scaricare](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier per Microsoft Visual Studio 2008/.NET Framework 3.5](/previous-versions/ms220948(v=vs.80))

    **Nota:** la Application Verifier disponibile in Visual Studio è piuttosto datata. Se possibile, usare invece il pacchetto autonomo. Per questo motivo, le versioni future Visual Studio non saranno più incorporate Application Verifier.

**WinQual:**

-   [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Segnalazione errori Windows: Attività iniziali](../wer/using-wer.md)

 

 
