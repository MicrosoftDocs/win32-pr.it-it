---
title: programmazione a 64 bit per sviluppatori di giochi
description: Questo articolo illustra i problemi di compatibilità e di portabilità e consente agli sviluppatori di semplificare la transizione a piattaforme a 64 bit.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e57ea1b3cc3272ca40465df31a04244d99e68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047065"
---
# <a name="64-bit-programming-for-game-developers"></a>programmazione a 64 bit per sviluppatori di giochi

I produttori di processori sono in esclusiva spedizione di processori a 64 bit nei propri computer desktop e anche i chipset della maggior parte dei computer portatili supportano la tecnologia x64. È importante per gli sviluppatori di giochi sfruttare i miglioramenti offerti dai processori a 64 bit con le nuove applicazioni e garantire che le applicazioni precedenti vengano eseguite correttamente sui nuovi processori e sulle edizioni a 64 bit di Windows Vista e Windows 7. Questo articolo illustra i problemi di compatibilità e di portabilità e consente agli sviluppatori di semplificare la transizione a piattaforme a 64 bit.

Microsoft dispone attualmente dei seguenti sistemi operativi a 64 bit:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (disponibile per gli OEM e per gli sviluppatori tramite MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 è disponibile solo come edizione a 64 bit.

 

-   [Differenze nella memoria indirizzabile](#differences-in-addressable-memory)
-   [Specifica di indirizzi di grandi dimensioni quando si compila](#specifying-large-address-aware-when-building)
-   [Compatibilità delle applicazioni a 32 bit su piattaforme a 64 bit](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Potenziali problemi di compatibilità](#potential-compatibility-pitfalls)
-   [Porting di applicazioni a piattaforme a 64 bit](#porting-applications-to-64-bit-platforms)
-   [Profilatura e ottimizzazione di applicazioni con porting](#profiling-and-optimization-of-ported-applications)
-   [Codice gestito in un sistema operativo a 64 bit](#managed-code-on-a-64-bit-operating-system)
-   [Implicazioni sulle prestazioni dell'esecuzione di un sistema operativo a 64 bit](#performance-implications-of-running-a-64-bit-operating-system)
-   [Summary](#summary)

## <a name="differences-in-addressable-memory"></a>Differenze nella memoria indirizzabile

La prima cosa che la maggior parte degli sviluppatori si nota è che i processori a 64 bit forniscono un notevole passo avanti nella quantità di memoria fisica e virtuale che può essere risolta.

-   le applicazioni a 32 bit su piattaforme a 32 bit possono indirizzare fino a 2 GB.
-   le applicazioni a 32 bit compilate con il flag del linker/LARGEADDRESSAWARE: Sì su Windows XP o Windows Server 2003 a 32 bit con l'opzione di avvio speciale/3GB possono essere indirizzate a un massimo di 3 GB. Questa operazione vincola il kernel solo a 1 GB, che può causare un errore di alcuni driver e/o servizi.
-   le applicazioni a 32 bit compilate con il flag del linker/LARGEADDRESSAWARE: Sì nelle edizioni a 32 bit di Windows Vista, Windows Server 2008 e Windows 7 possono indirizzare la memoria fino al numero specificato dall'elemento IncreaseUserVa dei dati di configurazione di avvio (BCD). Il valore predefinito di IncreaseUserVa può essere compreso tra 2048 e 3072 (che corrisponde alla quantità di memoria configurata dall'opzione di avvio/3GB in Windows XP). Il resto di 4 GB viene allocato al kernel e può causare la mancata configurazione di driver e servizi.

    Per ulteriori informazioni su BCD, vedere [dati configurazione di avvio](https://msdn.microsoft.com/library/aa362692.aspx) su MSDN.

-   le applicazioni a 32 bit su piattaforme a 64 bit possono indirizzare fino a 2 GB o fino a 4 GB con il flag del linker/LARGEADDRESSAWARE: Sì.
-   le applicazioni a 64 bit utilizzano 43 bit per l'indirizzamento, che fornisce 8 TB di indirizzo virtuale per le applicazioni e 8 TB riservati per il kernel.

Oltre alla semplice memoria, le applicazioni a 64 bit che utilizzano I/O di file mappati alla memoria traggono notevolmente vantaggio dallo spazio degli indirizzi virtuale più elevato. L'architettura a 64 bit ha anche migliorato le prestazioni a virgola mobile e il passaggio più rapido dei parametri. I processori a 64 bit hanno il doppio del numero di registri, sia dei tipi di utilizzo generico che di Streaming SIMD Extensions (SSE), oltre al supporto per i set di istruzioni SSE e SSE2. molti processori a 64 bit supportano anche set di istruzioni SSE3.

## <a name="specifying-large-address-aware-when-building"></a>Specifica di indirizzi di grandi dimensioni quando si compila

Quando si compilano applicazioni a 32 bit, è consigliabile specificare un indirizzo di grandi dimensioni, utilizzando il flag del linker/LARGEADDRESSAWARE, anche se l'applicazione non è destinata a una piattaforma a 64 bit, a causa dei vantaggi ottenuti senza costi aggiuntivi. Come spiegato in precedenza, l'abilitazione di questo flag per una compilazione consente a un programma a 32 bit di accedere a una quantità maggiore di memoria con opzioni di avvio speciali in un sistema operativo a 32 bit o in un sistema operativo a 64 bit. Tuttavia, gli sviluppatori devono prestare attenzione che i presupposti del puntatore non vengano eseguiti, ad esempio presumendo che l'alto bit non venga mai impostato in un puntatore a 32 bit. In generale, l'abilitazione del flag/LARGEADDRESSAWARE è una procedura consigliata.

Le applicazioni a 32 bit che sono compatibili con gli indirizzi grandi possono determinare in fase di esecuzione la quantità totale di spazio degli indirizzi virtuali disponibile con la configurazione del sistema operativo corrente chiamando [**GlobalMemoryStatusEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex). Il risultato di ullTotalVirtual è compreso tra 2147352576 byte (2 GB) e 4294836224 byte (4 GB). I valori maggiori di 3221094400 (3 GB) possono essere ottenuti solo nelle edizioni di Windows a 64 bit. Se, ad esempio, il valore di IncreaseUserVa è 2560, il risultato sarà ullTotalVirtual con un valore di 2684223488 byte.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Compatibilità delle applicazioni a 32 bit su piattaforme a 64 bit

I sistemi operativi Windows a 64 bit sono compatibili con l'architettura IA32 e la maggior parte delle API usate dalle applicazioni a 32 bit è disponibile tramite Windows 32-bit nell'emulatore Windows a 64 bit, WOW64. WOW64 contribuisce a garantire che queste API funzioneranno come previsto.

WOW64 dispone di un livello di esecuzione che gestisce il marshalling dei dati a 32 bit. WOW64 reindirizza le richieste di file DLL, reindirizza alcuni rami del registro di sistema per le applicazioni a 32 bit e riflette alcuni rami del registro di sistema per le applicazioni 32 e 64 bit.

Altre informazioni su WOW64 sono reperibili in [Dettagli di implementazione di WOW64](/windows/desktop/WinProg64/wow64-implementation-details) in MSDN. Per le procedure consigliate per la creazione di applicazioni eseguite in WOW64, vedere procedure consigliate [per WOW64](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) in Windows Hardware Developer Central.

### <a name="potential-compatibility-pitfalls"></a>Potenziali problemi di compatibilità

La maggior parte delle applicazioni sviluppate per una piattaforma a 32 bit viene eseguita senza problemi in una piattaforma a 64 bit. Alcune applicazioni potrebbero avere problemi, che possono includere quanto segue:

-   Tutti i driver per le edizioni a 64 bit dei sistemi operativi Windows devono essere versioni a 64 bit. La richiesta di nuovi driver a 64 bit presenta implicazioni per gli schemi di protezione da copia basati sui driver precedenti. Si noti che i driver in modalità kernel devono avere firma Authenticode per essere caricati da edizioni di Windows a 64 bit.
-   i processi a 64 bit non possono caricare DLL a 32 bit e i processi a 32 bit non possono caricare DLL a 64 bit. Prima di procedere con lo sviluppo, gli sviluppatori devono assicurarsi che siano disponibili versioni a 64 bit di dll di terze parti. Se è necessario usare una DLL a 32 bit in un processo a 64 bit, è possibile usare la comunicazione tra processi di Windows (IPC). I componenti COM possono inoltre utilizzare i server out-of-process e il marshalling per la comunicazione tra i limiti, ma ciò può comportare una riduzione delle prestazioni.
-   Molti processori x64 sono anche processori multicore e gli sviluppatori devono testare il modo in cui questo influiscono sulle applicazioni legacy. Altre informazioni sui processori multicore e sulle implicazioni per le applicazioni di gioco sono disponibili nei [processori di temporizzazione e multicore](/windows/desktop/DxTechArts/game-timing-and-multicore-processors).
-   Le applicazioni devono inoltre chiamare [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) per individuare i percorsi di file, in quanto alcuni nomi di cartella sono stati modificati in alcuni casi. Ad esempio, \_ i file di programma CSIDL \_ restituiranno "c: \\ Program Files (x86)" per un'applicazione a 32 bit in esecuzione su una piattaforma a 64 bit anziché "c: \\ Program Files". Gli sviluppatori devono essere consapevoli del funzionamento delle funzionalità di reindirizzamento e Reflection dell'emulatore WOW64.

Inoltre, gli sviluppatori devono diffidare dei programmi a 16 bit che potrebbero ancora usare. WOW64 non è in grado di gestire le applicazioni a 16 bit; sono inclusi i programmi di installazione obsoleti e tutti i programmi MS-DOS.

> [!Note]  
> I problemi di compatibilità più comuni sono i programmi di installazione che eseguono codice a 16 bit e non hanno driver a 64 bit per gli schemi di protezione della copia.

 

Nella sezione successiva vengono illustrati i problemi relativi al porting del codice a 64 bit nativo per gli sviluppatori che desiderano garantire il funzionamento dei programmi legacy sulle piattaforme a 64 bit. È anche per gli sviluppatori che non hanno familiarità con la programmazione a 64 bit.

## <a name="porting-applications-to-64-bit-platforms"></a>Porting di applicazioni a piattaforme a 64 bit

Con gli strumenti e le librerie appropriati è possibile semplificare la transizione dallo sviluppo a 32 bit a 64 bit. DirectX 9 SDK dispone di librerie per supportare i progetti basati su x86 e x64. Microsoft Visual Studio 2005 e Visual Studio 2008 supportano la generazione di codice sia per x86 che per x64 e sono forniti con librerie ottimizzate per la generazione di codice x64. Tuttavia, sarà anche necessario per gli sviluppatori distribuire i runtime di Visual C con le applicazioni. Si noti che le edizioni Express di Visual Studio 2005 e Visual Studio 2008 non includono il compilatore x64, ma le edizioni standard, Professional e Team System.

Gli sviluppatori destinati a piattaforme a 32 bit possono preparare lo sviluppo a 64 bit per semplificare la transizione in un secondo momento. Quando si compilano progetti a 32 bit, gli sviluppatori devono usare il flag/Wp64, che causerà la generazione di avvisi relativi a problemi che influiscono sulla portabilità. Il cambio a strumenti e librerie a 64 bit genererà inizialmente molti nuovi errori di compilazione. è quindi consigliabile cambiare gli strumenti e le librerie indipendenti da bit e correggere eventuali avvisi prima di passare a una compilazione a 64 bit.

Tuttavia, la modifica degli strumenti, la modifica delle librerie e l'utilizzo di determinati flag del compilatore non saranno sufficienti. È necessario rivalutare i presupposti negli standard di codifica per assicurarsi che gli standard di codifica correnti non consentano problemi di portabilità. I problemi di portabilità possono includere il troncamento del puntatore, le dimensioni e l'allineamento dei tipi di dati, la dipendenza da dll a 32 bit, l'uso di API legacy, codice assembly e file binari obsoleti.

> [!Note]  
> Visual C++ 2010 include le intestazioni stdint. h e cstdint C99 che definiscono i tipi di portabilità standard Int32 \_ t, UInt32 \_ t, Int64 \_ t, UInt64 \_ t, IntPtr t \_ e UIntPtr \_ t. L'uso di questi \_ tipi di dati, insieme ai tipi di dati ptrdiff t e size t, \_ può essere preferibile ai tipi portabilty di Windows usati di seguito per migliorare la portabilità del codice.

 

I principali problemi di porting includono i seguenti:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Troncamento puntatore**
</dt> <dd>

I puntatori sono 64 bit in un sistema operativo a 64 bit, quindi i puntatori di cast ad altri tipi di dati possono causare il troncamento e l'aritmetica dei puntatori può causare un danneggiamento. Se si usa il flag/Wp64, in genere viene visualizzato un avviso relativo a questo tipo di problema, ma l'uso di tipi polimorfici (INT \_ ptr, DWORD \_ ptr, Size \_ T, uint \_ ptr e così via) quando si esegue il cast dei tipi di puntatore è una procedura consigliata che consente di evitare il problema. Poiché i puntatori sono a 64 bit sulle nuove piattaforme, gli sviluppatori devono controllare l'ordine dei puntatori e i tipi di dati nelle classi e nelle strutture per ridurre o eliminare la spaziatura interna.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Tipi di dati e file binari**
</dt> <dd>

Sebbene i puntatori aumentino da 32 bit a 64 in una piattaforma a 64 bit, altri tipi di dati non lo sono. I tipi di dati a precisione fissa (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32, UINT64) possono essere utilizzati in posizioni in cui è necessario conoscere le dimensioni del tipo di dati. ad esempio, in una struttura di file binaria. Le modifiche alle dimensioni e all'allineamento dei dati del puntatore richiedono una gestione speciale per garantire la compatibilità da 32 bit a 64 bit. Altre informazioni sono reperibili in [preparazione per Windows a 64 bit: i nuovi tipi di dati](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**API Win32 e allineamento dati precedenti**
</dt> <dd>

Alcune API Win32 sono state deprecate e sostituite con chiamate API più neutre, ad esempio SetWindowLongPtr al posto di SetWindowLong.

La riduzione delle prestazioni per gli accessi non allineati è maggiore sulla piattaforma x64 rispetto a una piattaforma x86. È \_ possibile utilizzare le macro Alignment (t) e offset del campo \_ (t, Member) per determinare le informazioni di allineamento che possono essere utilizzate direttamente dal codice. L'uso corretto di queste macro suddette dovrebbe eliminare le potenziali penalità di accesso non allineate.

Altre informazioni sulla macro di \_ allineamento dei tipi, sulla macro di offset dei campi \_ e sulle informazioni di programmazione generali a 64 bit sono disponibili nella [programmazione Windows a 64 bit: suggerimenti per la migrazione: considerazioni aggiuntive](/windows/desktop/WinProg64/additional-considerations) e [preparazione per Windows a 64 bit: regole per l'utilizzo di puntatori](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Codice assembly**
</dt> <dd>

Il codice assembly inline non è supportato nelle piattaforme a 64 bit e deve essere sostituito. Le modifiche all'architettura potrebbero avere modificato i colli di bottiglia dell'applicazione e C/C++ o gli intrinseci possono ottenere risultati simili con codice più facile da leggere. La procedura più consigliata consiste nel passare tutto il codice assembly a C o C++. Gli intrinseci possono essere utilizzati al posto del codice dell'assembly, ma devono essere utilizzati solo dopo l'esecuzione della profilatura completa e dell'analisi.

X87, MMX e 3DNow! i set di istruzioni sono deprecati in modalità a 64 bit. I set di istruzioni sono ancora presenti per la compatibilità con le versioni precedenti per la modalità a 32 bit. Tuttavia, per evitare problemi di compatibilità in futuro, è sconsigliato l'uso nei progetti correnti e futuri.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**API deprecate**
</dt> <dd>

Alcune API DirectX obsolete sono state eliminate per le applicazioni native a 64 bit: DirectPlay 4 e versioni precedenti, DirectDraw 6 e versioni precedenti, Direct3D 8 e versioni precedenti e DirectInput 7 e versioni precedenti. Inoltre, l'API di base di DirectMusic è disponibile per le applicazioni native a 64 bit, ma il livello di prestazioni e il produttore DirectMusic sono deprecati.

Visual Studio rilascia avvisi di deprecazione e queste modifiche non rappresentano un problema per gli sviluppatori che usano le API più recenti.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Profilatura e ottimizzazione di applicazioni con porting

Tutti gli sviluppatori devono riprofilare tutte le applicazioni che vengono trasferite a nuove architetture. Molte applicazioni che vengono trasferite a piattaforme a 64 bit avranno profili di prestazioni diversi dalle versioni a 32 bit. Gli sviluppatori devono eseguire test delle prestazioni a 64 bit prima di valutare gli elementi che devono essere ottimizzati. L'aspetto positivo è che molte ottimizzazioni tradizionali funzionano su piattaforme a 64 bit. Inoltre, i compilatori a 64 bit possono anche eseguire numerose ottimizzazioni con l'uso corretto dei flag del compilatore e degli hint di codifica.

Alcune strutture possono avere tipi di dati interni riordinati per conservare lo spazio di memoria e migliorare la memorizzazione nella cache. In alcuni casi, è possibile usare gli indici di matrice al posto di un puntatore a 64 bit completo. Il flag/FP: Fast può migliorare l'ottimizzazione e la vettorizzazione a virgola mobile. \_ \_ L'uso di Restrict, declspec (restrict) e declspec (noalias) può aiutare il compilatore a risolvere gli alias e a migliorare l'uso del file di registro.

Altre informazioni su/FP: Fast sono disponibili in [/FP (specificare il comportamento di Floating-Point)](/cpp/build/reference/fp-specify-floating-point-behavior).

Altre informazioni sulla \_ \_ limitazione sono reperibili in [modificatori specifici di Microsoft](/cpp/cpp/microsoft-specific-modifiers).

Altre informazioni su declspec (restrict) sono disponibili in [procedure consigliate](/cpp/build/optimization-best-practices)per l'ottimizzazione.

Altre informazioni su declspec (noalias) sono reperibili in [ \_ \_ declspec (noalias)](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx).

## <a name="managed-code-on-a-64-bit-operating-system"></a>Codice gestito in un sistema operativo a 64 bit

Il codice gestito viene usato da molti sviluppatori di giochi nella rispettiva catena di strumenti, quindi è utile comprendere il comportamento di un sistema operativo a 64 bit. Il codice gestito è un set di istruzioni neutro. Pertanto, quando si esegue un'applicazione gestita in un sistema operativo a 64 bit, Common Language Runtime (CLR) può eseguirlo come processo a 32 o a 64 bit. Per impostazione predefinita, CLR esegue le applicazioni gestite come 64 bit e dovrebbero funzionare correttamente senza problemi. Tuttavia, se l'applicazione dipende da una DLL nativa a 32 bit, l'applicazione avrà esito negativo quando tenterà di chiamare la DLL. Un processo a 64 bit richiede codice completamente a 64 bit e non è possibile chiamare una DLL a 32 bit da un processo a 64 bit. La soluzione migliore a lungo termine consiste nel compilare il codice nativo anche come 64 bit, ma una soluzione perfettamente ragionevole a breve termine è semplicemente contrassegnare l'applicazione gestita come per x86 solo usando il flag di compilazione/Platform: x86.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Implicazioni sulle prestazioni dell'esecuzione di un sistema operativo a 64 bit

Poiché i processori con l'architettura AMD64 e Intel 64 possono eseguire istruzioni a 32 bit a livello nativo, possono eseguire applicazioni a 32 bit a velocità intera, anche in un sistema operativo a 64 bit. È previsto un costo modesto per la conversione di parametri tra 32 bit e 64 bit quando si chiamano funzioni del sistema operativo, ma questo costo è generalmente irrilevante. Ciò significa che non si verifica alcun rallentamento quando si eseguono applicazioni a 32 bit in un sistema operativo a 64 bit.

Quando si compilano applicazioni come 64 bit, i calcoli risultano più complessi. Un programma a 64 bit usa puntatori a 64 bit e le istruzioni sono leggermente più grandi, quindi il requisito di memoria è leggermente maggiore. Questo può causare una lieve riduzione delle prestazioni. D'altra parte, il doppio dei registri e la possibilità di eseguire calcoli di interi a 64 bit in un'unica istruzione spesso sono più che compensano. Il risultato finale è che un'applicazione a 64 bit può essere eseguita leggermente più lentamente rispetto alla stessa applicazione compilata come 32 bit, ma viene spesso eseguita leggermente più velocemente.

## <a name="summary"></a>Riepilogo

Le architetture a 64 bit consentono agli sviluppatori di effettuare il push delle limitazioni relative all'aspetto, al suono e alla riproduzione dei giochi. Tuttavia, la transizione dalla programmazione a 32 bit alla programmazione a 64 bit non è semplice. Comprendendo le differenze tra i due e usando gli strumenti più recenti, la transizione alle piattaforme a 64 bit può essere più semplice e veloce.

Altre informazioni sulla programmazione a 64 bit sono disponibili in [Visual C++ Developer Center: programmazione a 64 bit](https://msdn.microsoft.com/vstudio//aa336463.aspx).

 

 