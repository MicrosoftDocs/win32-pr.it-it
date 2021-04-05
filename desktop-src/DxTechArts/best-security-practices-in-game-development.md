---
title: Procedure di sicurezza consigliate per lo sviluppo di giochi
description: Questo articolo illustra le procedure consigliate da usare nello sviluppo di giochi.
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba4f02d5e1a2e3da2e50feedd89f085a0c063be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872698"
---
# <a name="best-security-practices-in-game-development"></a>Procedure di sicurezza consigliate per lo sviluppo di giochi

Questo articolo illustra le procedure consigliate da usare nello sviluppo di giochi.

-   [Introduzione](#introduction)
-   [Esempi di codice non sicuro](#examples-of-insecure-code)
-   [Modi per migliorare la sicurezza](#ways-to-improve-security)
-   [Summary](#summary)

## <a name="introduction"></a>Introduzione

Un numero crescente di persone Gioca giochi online e giochi con contenuti creati dall'utente. Questo, combinato con la maggiore sicurezza del sistema operativo Microsoft Windows, significa che i giochi sono una destinazione sempre più accattivante per gli attacchi da sfruttare. Gli sviluppatori di giochi devono dare un'enfasi forte per assicurarsi che i giochi da loro rilasciati non creino nuovi problemi di sicurezza da sfruttare per gli utenti malintenzionati. Gli sviluppatori di giochi hanno una responsabilità e un interesse per impedire ai computer dei clienti di essere compromessi da dati di rete dannosi, modifiche dell'utente o manomissioni. Se una vulnerabilità viene sfruttata, potrebbe causare la perdita di clienti e/o denaro. Questo articolo illustra alcuni metodi e strumenti comuni per aumentare la sicurezza del codice senza ingrandire i tempi di sviluppo.

I tre errori più comuni compiuti da un team di sviluppo durante il rilascio di un prodotto sono:

-   Richiesta dei privilegi amministrativi. I giochi non devono richiedere privilegi amministrativi. Per altri dettagli, vedere [controllo dell'account utente per sviluppatori di giochi](./user-account-control-for-game-developers.md).
-   Non viene usata la protezione automatica. Gli sviluppatori in genere non usano **/GS**, **/SAFESEH** o **/NX**. Usando questi flag di compilazione/collegamento è possibile individuare o eliminare molti buchi di sicurezza di base senza aumentare significativamente il carico di lavoro. Questi flag vengono descritti più avanti in questo articolo.
-   Uso di API non consentite. Sono disponibili molte API (**strcpy**, **strncpy** e così via) soggette a errori del programmatore e generano facilmente buchi di sicurezza. Gli sviluppatori devono sostituire queste API con le versioni sicure. Visual Studio 2005 è dotato di uno strumento per l'analisi di file binari che consentono di controllare automaticamente i file oggetto per i riferimenti a API non sicure. Per altre informazioni sulle operazioni da eseguire con le informazioni generate con questo strumento, vedere [respingere gli attacchi sul codice con le librerie C e C++ sicure di Visual Studio 2005](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) di Martyn Lovell. Inoltre, è possibile ottenere il file di intestazione [. h vietato](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) che consente di rimuovere le funzioni vietate dal codice.

Ognuno degli errori elencati non è solo comune, ma è facilmente correggibile senza modifiche significative nel carico di lavoro di sviluppo, negli standard di codifica o nelle funzionalità.

## <a name="examples-of-insecure-code"></a>Esempi di codice non sicuro

Di seguito è riportato un semplice esempio di tutto il necessario per consentire a un utente malintenzionato di eseguire un attacco di sovraccarico del buffer:


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



All'apparenza, il codice è OK: chiama una funzione sicura, dopo tutto. I dati della rete vengono copiati in un buffer di 256 byte. La funzione **strncpy** si basa sulla ricerca di un carattere di terminazione null nella stringa di origine o è limitato dal numero di buffer specificato. Il problema è che le dimensioni del buffer non sono corrette. Se i dati provenienti dalla rete non vengono convalidati o se la dimensione del buffer non è corretta (come in questo esempio), un utente malintenzionato potrebbe semplicemente fornire un buffer di grandi dimensioni per sovrascrivere i dati dello stack, al termine del buffer, con i dati nel pacchetto di rete. Ciò consente all'autore dell'attacco di eseguire codice arbitrario sovrascrivendo il puntatore all'istruzione e modificando l'indirizzo di ritorno. La lezione più elementare di questo esempio consiste nel non considerare mai attendibile l'input fino a quando non viene verificato.

Anche se i dati non provengono inizialmente dalla rete, esiste comunque un rischio potenziale. Lo sviluppo di giochi moderni richiede molti utenti che progettano, sviluppano e testano la stessa codebase. Non esiste alcun modo per capire come verrà chiamata la funzione in futuro. Sempre chiedersi da dove provengono i dati e che cosa potrebbe controllare un utente malintenzionato? Sebbene gli attacchi basati sulla rete siano i più comuni, non sono gli unici metodi per creare buchi di sicurezza. Un utente malintenzionato può creare un mod o modificare un file salvato in modo da aprire un problema di sicurezza? Quali sono i file audio e di immagine forniti dall'utente? Le versioni dannose di questi file potrebbero essere pubblicate su Internet e creare rischi di sicurezza pericolosi per i clienti.

Come nota secondaria, usare strsafe. h o CRT sicuro anziché **strncpy** per correggere l'esempio. CRT sicuro è una revisione completa della sicurezza del runtime C ed è incluso in Visual Studio 2005. Altre informazioni sulla libreria CRT sicura sono disponibili in [miglioramenti della sicurezza in CRT](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) di Michael Howard.

## <a name="ways-to-improve-security"></a>Modi per migliorare la sicurezza

Esistono diversi modi per migliorare la sicurezza del ciclo di sviluppo. Ecco alcuni dei modi migliori:

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>Lettura della sicurezza
</dt> <dd>

Il libro *scrittura di codice sicuro, seconda edizione* di Michael Howard e David LeBlanc, fornisce una spiegazione approfondita e chiara delle strategie e dei metodi di prevenzione degli attacchi e mitigazione degli exploit. Iniziando con i metodi di progettazione della sicurezza in una versione per le tecniche per la protezione delle applicazioni di rete, il libro copre tutti gli aspetti che uno sviluppatore di giochi deve aiutare a proteggere se stesso, i prodotti e i clienti da utenti malintenzionati. Il libro può essere usato per infondere le impostazioni cultura di sicurezza in uno sviluppo studio. Non basta pensare alla sicurezza del codice come problema di uno sviluppatore o a un problema del tester. Si pensi alla sicurezza come a un intero team, dal Program Manager alla progettazione fino allo sviluppo a tester, da considerare quando lavorano su un progetto. Più gli occhi che fanno parte del processo di revisione, maggiore è la probabilità di intercettare un problema di sicurezza prima del rilascio.

La *scrittura di codice sicuro, seconda edizione* si trova in [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) e informazioni di sicurezza più generali sono disponibili per evitare [attacchi futuri riducendo la superficie di attacco](/previous-versions/ms972812(v=msdn.10)) di Michael Howard.

Michael Howard, David LeBlanc e John esclusivamente ganasce Viega hanno scritto un altro libro sull'argomento che copre tutti i sistemi operativi e i linguaggi di programmazione comuni, che hanno diritto a *19 peccati letali di sicurezza del software*.

Le presentazioni sulla sicurezza incentrate sui giochi sono disponibili nella pagina di download delle [presentazioni per sviluppatori Microsoft XNA](/previous-versions/dn629515(v=msdn.10)) .

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>Analisi della modellazione delle minacce
</dt> <dd>

Un'analisi di modellazione delle minacce è un modo efficace per valutare la sicurezza del sistema, non in un linguaggio specifico o usando uno strumento, ma in un ampio metodo end-to-end che può essere eseguito in alcune riunioni. Una volta implementato correttamente, un modello di thread può identificare tutti i punti di forza e i punti deboli di un sistema, senza aggiungere un carico di lavoro o un tempo di riunione significativo al progetto. Il metodo di modellazione delle minacce mette in evidenza anche la valutazione della sicurezza del sistema prima e durante il processo di sviluppo, in modo da garantire che venga eseguita una valutazione completa concentrandosi sulle funzionalità più rischiose. Può essere considerato come un profiler per la sicurezza. Poiché non si basa su una lingua specifica o si basa su uno strumento specifico, la modellazione delle minacce può essere usata in qualsiasi studio di sviluppo che lavora su qualsiasi progetto di qualsiasi genere. La modellazione delle minacce è anche un ottimo metodo per rinforzare l'idea che la sicurezza è responsabilità di tutti e non di altri.

Quando si esegue la modellazione delle minacce, prestare particolare attenzione a:

-   Origini dati UDP
-   Origini dati che non richiedono l'autenticazione
-   Origini dati di cui viene eseguita la ricerca frequente e in genere come parte della raccolta di informazioni su larga scala
-   Qualsiasi capacità di un client di inviare direttamente i dati ad altri client

Queste sono le aree che hanno un potenziale rischio di debolezza della sicurezza.

Per ulteriori informazioni sulla modellazione delle minacce, vedere la [pagina relativa alla modellazione](https://technet.microsoft.com/security/) delle minacce in MSDN Security Development Center e nel libro [Threat Modeling](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) di Frank Swiderski e Window Snyder.

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>Protezione esecuzione programmi (/NX)
</dt> <dd>

Uno strumento recente per attenuare più exploit è la protezione esecuzione programmi (DEP, Data Execution Prevention). Se si include l'opzione **/NX** nel comando Build, Visual Studio contrassegna le pagine di memoria con flag che indicano se il codice ha il diritto di eseguire o meno. Qualsiasi programma che tenta di eseguire in una pagina di memoria non contrassegnata con l'autorizzazione EXECUTE provocherà una terminazione forzata del programma. La prevenzione viene applicata a livello di processore e influirà sugli sviluppatori che usano il codice di modifica automatica o i compilatori di linguaggio JIT nativi. Attualmente, solo i processori Athlon64 e Opteron di AMD e i processori Intel Itanium e più recenti Pentium 4 supportano la prevenzione dell'esecuzione, ma si prevede che tutti i processori a 32 bit e a 64 bit supporteranno la prevenzione dell'esecuzione in futuro. Uno schema di protezione da copia utilizzato da uno sviluppatore potrebbe essere interessato dalla prevenzione dell'esecuzione, ma Microsoft ha collaborato con i fornitori della protezione delle copie per ridurre al minimo l'impatto. È consigliabile utilizzare DEP.

Per altri dettagli su DEP, vedere [prevenzione dell'esecuzione dei dati](../memory/data-execution-prevention.md).

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>Il controllo di sicurezza del buffer (/GS) e l'immagine hanno gestori di eccezioni sicure (/SAFESEH)
</dt> <dd>

Il *controllo di sicurezza del buffer*, specificato dal flag del compilatore **/GS** e l' *immagine ha gestori delle eccezioni sicuri*, specificati dal flag del linker **/SAFESEH** (per la prima volta implementato in Visual Studio .NET 2003), può rendere più semplice la protezione del codice da parte dello sviluppatore.

L'utilizzo del flag **/GS** fa sì che il compilatore costruisca un controllo per alcune forme di sovraccarichi del buffer basati su stack che potrebbero essere sfruttati per sovrascrivere l'indirizzo di ritorno di una funzione. L'uso di **/GS** non rileva ogni potenziale sovraccarico del buffer e non deve essere considerato un catch-all, ma una efficace tecnologia di difesa in profondità.

L'utilizzo del flag **/SAFESEH** indicherà al linker di generare solo un eseguibile o una dll se può generare anche una tabella dei gestori di eccezioni sicure del file eseguibile o della dll. La gestione delle eccezioni strutturate sicure (SafeSEH) Elimina la gestione delle eccezioni come destinazione degli attacchi di sovraccarico del buffer garantendo che, prima dell'invio di un'eccezione, il gestore di eccezioni venga registrato nella tabella delle funzioni che si trova all'interno del file di immagine. Questi vantaggi di protezione sono abilitati con Windows XP SP2, Windows Server 2003, Windows Vista e Windows 7. Inoltre, per il corretto funzionamento di **/SAFESEH** , è necessario utilizzarlo in un metodo All-or-Nothing. Tutte le librerie che contengono codice associato a un file eseguibile o a una DLL devono essere compilate con **/SAFESEH** o la tabella non verrà generata.

Altre informazioni sul [controllo di sicurezza del buffer](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) (**/GS**) e sull' [immagine hanno gestori di eccezioni sicure](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) (**/SAFESEH**) sono reperibili in MSDN.

Vedere anche informazioni sul [flag **/SDL**](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019) di Microsoft Visual Studio 2012 e sui miglioramenti apportati a Visual Studio 2012 [per il flag **/GS**](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/).

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

PREfast è uno strumento gratuito offerto da Microsoft che analizza i percorsi di esecuzione in C o C++ compilato per individuare i bug in fase di esecuzione. La funzione PREfast opera attraverso tutti i percorsi di esecuzione in tutte le funzioni e la valutazione di ogni percorso per individuare eventuali problemi. Usato originariamente per sviluppare driver e altro codice kernel, questo strumento può aiutare gli sviluppatori di giochi a risparmiare tempo eliminando alcuni bug difficili da trovare o ignorati dal compilatore. L'uso di PREfast è un ottimo modo per ridurre il carico di lavoro e concentrare gli sforzi del team di sviluppo e del team di test. PREfast è disponibile in Visual Studio Team Suite e Visual Studio Team Edition for Software Developers come analisi codice, abilitata dall'opzione del compilatore **/Analyze**. Questa opzione è disponibile anche nella versione gratuita del compilatore fornita con Windows Software Development Kit.

> [!Note]  
> Visual Studio 2012 supporta **/Analyze** in tutte le edizioni. Per ulteriori informazioni sulla disponibilità dell'analisi del codice in tutte le edizioni di Visual Studio, vedere Novità di [analisi codice](/archive/blogs/codeanalysis/?m=20123).

 

Tramite l'uso dell'annotazione di intestazione (in particolare per gli argomenti del puntatore del buffer), PREfast può esporre problemi aggiuntivi, ad esempio bug di sovrascrittura della memoria, un'origine comune di arresti anomali e potenziali vulnerabilità della sicurezza. Questa operazione viene eseguita usando il linguaggio di annotazione standard (SAL), che è una forma di contrassegno per i prototipi di funzione C/C++ che forniscono informazioni aggiuntive sulla semantica degli argomenti del puntatore prevista e sulla correlazione con parametri di lunghezza, dimensioni del buffer dichiarate e così via. Tutte le intestazioni per i sistemi operativi Windows sono annotate e l'aggiunta di SAL Mark-up nelle intestazioni API pubbliche nelle librerie personalizzate consente di eseguire in modo rapido controlli più dettagliati e aggressivi nel codice client per tali API. Per un'introduzione a SAL e collegamenti ad altre informazioni, vedere il post del Blog di Michael Howard, "[una breve introduzione al linguaggio di annotazione standard (SAL)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)".

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>Application Verifier di Windows
</dt> <dd>

Windows Application Verifier, o AppVerifier, può aiutare i tester fornendo più funzioni in uno strumento. AppVerifier è uno strumento sviluppato per rendere più testabili gli errori di programmazione comuni. AppVerifier può controllare i parametri passati alle chiamate API, inserire input errato per verificare la capacità di gestione degli errori e registrare le modifiche al registro di sistema e file system. AppVerifier è anche in grado di rilevare i sovraccarichi del buffer nell'heap, verificare che un elenco di controllo di accesso (ACL) sia stato definito correttamente e imporre l'uso sicuro delle API socket. Sebbene non esaustivo, AppVerifier può essere uno strumento nella casella degli strumenti del tester per aiutare un prodotto di sviluppo a rilasciare un prodotto di qualità.

Per ulteriori informazioni su Application Verifier, vedere [Application Verifier](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) e [utilizzo di Application Verifier all'interno del ciclo](/previous-versions/aa480483(v=msdn.10)) di vita di sviluppo del software su MSDN.

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>Test fuzzy
</dt> <dd>

Il *test fuzzy* è un metodo di test semi-automatizzato che può migliorare le metodologie di testing correnti. L'idea centrale dietro i test fuzzy consiste nel eseguire una valutazione completa di tutti gli input inserendo dati casuali per visualizzare le interruzioni. sono inclusi tutti i dati di rete, i mods e i giochi salvati e così via. Il test fuzzy è piuttosto semplice. È sufficiente modificare i file o i dati di rete ben formati inserendo byte casuali, capovolgendo byte adiacenti o negando valori numerici. 0xFF, 0xFFFF, 0xFFFFFFFF, 0x00, 0x0000, 0x00000000 e 0x80000000 sono valori validi per l'esposizione di buchi di sicurezza durante i test fuzzy. È possibile osservare le combinazioni di interazioni risultanti usando AppVerifier. Sebbene il fuzzing non sia esaustivo, è facile da implementare e automatizzare e può rilevare i bug più elusivi e imprevedibili.

Per ulteriori informazioni sui test di Fuzz, vedere la pagina relativa alla *procedura pratica relativa alla sicurezza dei giochi in* [Gamefest 2007](/previous-versions/dn629515(v=msdn.10)) .

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Firma Authenticode
</dt> <dd>

Authenticode è un metodo per garantire che i file eseguibili, i file DLL e i pacchetti di Windows Installer (file con estensione msi) ricevuti dall'utente non vengano modificati da quelli rilasciati da uno sviluppatore. Utilizzando una combinazione di principi crittografici, entità attendibili e standard di settore, Authenticode verifica l'integrità del contenuto eseguibile. Microsoft fornisce un'API di crittografia, CryptoAPI, che può essere usata per rilevare automaticamente eventuali manomissioni del codice firmato. Se si verifica una perdita di sicurezza dopo una versione, un certificato può essere revocato e tutto il codice firmato con tale certificato smetterà di eseguire l'autenticazione. Con la revoca di un certificato, la convalida di tutti i titoli firmati con il certificato viene revocata. Windows è stato progettato per funzionare con la firma Authenticode e avvisa un utente del codice non firmato, in situazioni specifiche, che potrebbe esporre il PC di un utente ad attacchi.

Authenticode non deve essere considerato un metodo per eliminare i problemi di sicurezza, ma un metodo per rilevare eventuali manomissioni dopo il rilascio di un file eseguibile. Un eseguibile o una DLL che contiene un problema di sicurezza sfruttabile può essere firmato e verificato tramite Authenticode, ma il problema di sicurezza verrà comunque introdotto nel nuovo sistema. Solo dopo la verifica della sicurezza di un prodotto o di un aggiornamento, il codice deve essere firmato per garantire agli utenti che dispongono di una versione che non è stata manomessa.

Anche se uno sviluppatore ritiene che non esista alcuna minaccia per la modifica delle versioni, altre tecnologie e servizi si basano su Authenticode. La firma del codice è facile da integrare e automatizzare; non esiste alcun motivo per cui gli sviluppatori non abbiano firmato le versioni.

Per ulteriori informazioni sulla firma Authenticode, vedere [firma Authenticode per sviluppatori di giochi](./authenticode-signing-for-game-developers.md).

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>Riduci privilegi
</dt> <dd>

Nei processi generali deve essere eseguito con il set minimo di privilegi necessari per operare. In Windows Vista e Windows 7 questa operazione viene eseguita tramite il [controllo dell'account utente](./user-account-control-for-game-developers.md), consentendo al gioco di essere eseguito come utente standard anziché come amministratore. Per Windows XP, in genere i giochi vengono sempre eseguiti come amministratore. Anche in Windows Vista e Windows 7 è talvolta necessario elevare i diritti di amministratore completo per alcune operazioni specifiche.

Nei casi in cui il processo è in esecuzione con diritti amministrativi completi, in genere sono necessari solo alcuni diritti oltre a quelli di un utente standard. L'accesso amministrativo include molti diritti non richiesti dal codice legittimo, ma che potrebbero essere usati da un utente malintenzionato, con una certa debolezza nel processo. Esempi di questi diritti includono SE \_ Take \_ ownership, se il \_ debug, se \_ Create \_ token, se \_ ASSIGNPRIMARYTOKEN, se \_ TCB, SE \_ Security, se \_ Load \_ driver, SE \_ SYSTEMTIME, se \_ backup, se \_ Restore, se \_ Shutdown e se \_ audit (vedere [costanti privilegio](../secauthz/privilege-constants.md)).

Sebbene un processo non possa ottenere più diritti dopo l'avvio, può facilmente concedere diritti. All'avvio, il processo può utilizzare immediatamente le API Win32 per rimuovere i diritti non richiesti.

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>Usare le funzionalità di sicurezza di Windows
</dt> <dd>

Windows Vista e Windows 7 includono numerose nuove funzionalità che migliorano la sicurezza del codice. Il [controllo dell'account utente](./user-account-control-for-game-developers.md) è certamente l'aspetto più importante da comprendere e adottare, ma sono disponibili anche altre funzionalità. Oltre alle tecnologie di Windows XP SP2, ad esempio la Windows Firewall, la prevenzione dell'esecuzione dei dati, il controllo della sicurezza del buffer e i gestori di eccezioni sicure, disponibili anche in Windows Vista e Windows 7, sono disponibili tre nuove funzionalità di sicurezza da considerare:

-   Funzionalità di sequenza casuale del layout dello spazio degli indirizzi esplicito. Questa funzionalità è abilitata mediante il collegamento con l'opzione **/DynamicBase** in visual Studio 2005 Service Pack 1 o visual Studio 2008. In questo modo il sistema rende casuale le posizioni di molte delle DLL di sistema principali nello spazio del processo, rendendo molto più difficile la scrittura di programmi di attacco sfruttabili che si propagano su larga scala in Internet. Questo flag del linker viene ignorato da Windows XP e dalle versioni precedenti di Windows.
-   Il danneggiamento dell'heap può causare un'intera classe di exploit di sicurezza, pertanto il sistema di memoria di Windows Vista e Windows 7 supporta ora una modalità che termina il processo se viene rilevato un danneggiamento dell'heap. La chiamata di [**HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation) con **HeapEnableTermianteOnCorruption** consentirà di acconsentire esplicitamente a questo comportamento. Questa chiamata ha esito negativo in Windows XP e nelle versioni precedenti di Windows.
-   Quando si scrivono i servizi, è possibile configurarli usando una nuova funzionalità per specificare quali privilegi sono effettivamente necessari, nonché per limitare l'accesso alle risorse a un SID specifico. Questa operazione viene eseguita tramite [ChangeSeviceConfig2](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a), usando le informazioni sui privilegi richiesti per la configurazione del servizio e il servizio \_ \_ \_ \_ \_ configurazione servizio \_ \_ \_ info SID.

</dd> </dl>

## <a name="summary"></a>Riepilogo

Lo sviluppo di un gioco per il Marketplace attuale e futuro è costoso e dispendioso in termini di tempo. Il rilascio di un gioco con problemi di sicurezza comporta un costo maggiore per la corretta correzione. Quindi, gli sviluppatori di giochi possono integrare gli strumenti e le tecniche per mitigare gli exploit di sicurezza prima del rilascio.

Le informazioni contenute in questo articolo sono solo un'introduzione a ciò che può fare un studio di sviluppo per aiutare se stessi e i loro clienti. Altre informazioni sulle procedure di sicurezza generali e informazioni sulla sicurezza sono disponibili in [Microsoft Security Developer Center](https://technet.microsoft.com/security/).

 

 