---
title: Programmazione a 64 bit per sviluppatori di giochi
description: Questo articolo illustra i problemi di compatibilità e portabilità e consente agli sviluppatori di semplificare la transizione alle piattaforme a 64 bit.
ms.assetid: 23a7ed41-6637-0607-327e-983b622e9104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439db3173e18206cb04875ab9c4422dbcedc7230508c8e98cf09b7fe27bfb9f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042431"
---
# <a name="64-bit-programming-for-game-developers"></a>Programmazione a 64 bit per sviluppatori di giochi

I produttori di processori spedino esclusivamente processori a 64 bit nei computer desktop e anche i chipset della maggior parte dei computer portatili supportano la tecnologia x64. È importante per gli sviluppatori di giochi sfruttare i miglioramenti offerti dai processori a 64 bit con le nuove applicazioni e assicurarsi che le applicazioni precedenti vengano eseguite correttamente nei nuovi processori e nelle edizioni a 64 bit di Windows Vista e Windows 7. Questo articolo illustra i problemi di compatibilità e portabilità e consente agli sviluppatori di semplificare la transizione alle piattaforme a 64 bit.

Microsoft attualmente dispone dei sistemi operativi a 64 bit seguenti:

-   Windows Server 2003 Service Pack 1
-   Windows XP Professional x64 Edition (disponibile per gli OEM e per gli sviluppatori tramite MSDN)
-   Windows Vista
-   Windows Server 2008
-   Windows 7
-   Windows Server 2008 R2

> [!Note]  
> Windows Server 2008 R2 è disponibile solo come edizione a 64 bit.

 

-   [Differenze nella memoria indirizzabile](#differences-in-addressable-memory)
-   [Specifica di un indirizzo di grandi dimensioni durante la compilazione](#specifying-large-address-aware-when-building)
-   [Compatibilità delle applicazioni a 32 bit su piattaforme a 64 bit](#compatibility-of-32-bit-applications-on-64-bit-platforms)
    -   [Potenziali problemi di compatibilità](#potential-compatibility-pitfalls)
-   [Porting di applicazioni su piattaforme a 64 bit](#porting-applications-to-64-bit-platforms)
-   [Profilatura e ottimizzazione delle applicazioni portate](#profiling-and-optimization-of-ported-applications)
-   [Codice gestito in un sistema operativo a 64 bit](#managed-code-on-a-64-bit-operating-system)
-   [Implicazioni relative alle prestazioni dell'esecuzione di un sistema operativo a 64 bit](#performance-implications-of-running-a-64-bit-operating-system)
-   [Summary](#summary)

## <a name="differences-in-addressable-memory"></a>Differenze nella memoria indirizzabile

La prima cosa che la maggior parte degli sviluppatori nota è che i processori a 64 bit offrono un notevole passo avanti nella quantità di memoria fisica e virtuale che è possibile risolvere.

-   Le applicazioni a 32 bit su piattaforme a 32 bit possono essere indirizzate fino a 2 GB.
-   Le applicazioni a 32 bit compilate con il flag del linker /LARGEADDRESSAWARE:YES in Windows XP o Windows Server 2003 a 32 bit con l'opzione di avvio speciale /3gb possono risolvere fino a 3 GB. In questo modo il kernel viene vincolato a 1 GB e ciò può causare l'errore di alcuni driver e/o servizi.
-   Le applicazioni a 32 bit compilate con il flag del linker /LARGEADDRESSAWARE:YES nelle edizioni a 32 bit di Windows Vista, Windows Server 2008 e Windows 7 possono risolvere la memoria fino al numero specificato dall'elemento dei dati di configurazione di avvio (BCD) IncreaseUserVa. IncreaseUserVa può avere un valore compreso tra 2048, il valore predefinito, e 3072 (che corrisponde alla quantità di memoria configurata dall'opzione di avvio /3gb in Windows XP). Il resto di 4 GB viene allocato al kernel e può causare errori nelle configurazioni di driver e servizi.

    Per altre informazioni su BCD, [vedere](https://msdn.microsoft.com/library/aa362692.aspx) dati configurazione di avvio su MSDN.

-   Le applicazioni a 32 bit su piattaforme a 64 bit possono essere indirizzate fino a 2 GB o fino a 4 GB con il flag del linker /LARGEADDRESSAWARE:YES.
-   Le applicazioni a 64 bit usano 43 bit per l'indirizzamento, che fornisce 8 TB di indirizzi virtuali per le applicazioni e 8 TB riservati per il kernel.

Oltre alla memoria, le applicazioni a 64 bit che usano I/O di file mappati alla memoria traggono grandi vantaggi dall'aumento dello spazio degli indirizzi virtuali. L'architettura a 64 bit offre anche prestazioni a virgola mobile migliorate e un passaggio più rapido dei parametri. I processori a 64 bit hanno il doppio del numero di registri, sia di tipi SSE (General Purpose and Streaming SIMD Extensions), sia di set di istruzioni SSE e SSE2. molti processori a 64 bit supportano anche set di istruzioni SSE3.

## <a name="specifying-large-address-aware-when-building"></a>Specifica di un indirizzo di grandi dimensioni durante la compilazione

È consigliabile specificare il supporto di indirizzi di grandi dimensioni durante la compilazione di applicazioni a 32 bit, usando il flag del linker /LARGEADDRESSAWARE, anche se l'applicazione non è destinata a una piattaforma a 64 bit, a causa dei vantaggi che vengono ottenuti senza alcun costo. Come spiegato in precedenza, l'abilitazione di questo flag per una compilazione consente a un programma a 32 bit di accedere a più memoria con opzioni di avvio speciali in un sistema operativo a 32 bit o in un sistema operativo a 64 bit. Tuttavia, gli sviluppatori devono prestare attenzione a non fare ipotesi sul puntatore, ad esempio supponendo che il bit alto non sia mai impostato in un puntatore a 32 bit. In generale, è consigliabile abilitare il flag /LARGEADDRESSAWARE.

Le applicazioni a 32 bit che sono in grado di riconoscere gli indirizzi di grandi dimensioni possono determinare in fase di esecuzione la quantità totale di spazio degli indirizzi virtuali disponibile con la configurazione corrente del sistema operativo chiamando [**GlobalMemoryStatusEx.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) Il risultato di ullTotalVirtual va da 2147352576 byte (2 GB) a 4294836224 byte (4 GB). I valori maggiori di 3221094400 (3 GB) possono essere ottenuti solo nelle edizioni a 64 bit di Windows. Ad esempio, se IncreaseUserVa ha un valore di 2560, il risultato è ullTotalVirtual con un valore di 2684223488 byte.

## <a name="compatibility-of-32-bit-applications-on-64-bit-platforms"></a>Compatibilità delle applicazioni a 32 bit su piattaforme a 64 bit

I sistemi operativi Windows a 64 bit sono compatibili a livello binario con l'architettura IA32 e la maggior parte delle API usate dalle applicazioni a 32 bit è disponibile tramite Windows Windows Windows Emulator a 64 bit, WOW64. WOW64 garantisce che queste API funzionino come previsto.

WOW64 ha un livello di esecuzione che gestisce il marshalling dei dati a 32 bit. WOW64 reindirizza le richieste di file DLL, reindirizza alcuni rami del Registro di sistema per le applicazioni a 32 bit e riflette alcuni rami del Registro di sistema per le applicazioni a 32 e a 64 bit.

Per altre informazioni su WOW64, vedere Dettagli [sull'implementazione di WOW64](/windows/desktop/WinProg64/wow64-implementation-details) in MSDN. Per le procedure consigliate per la compilazione di applicazioni eseguite in WOW64, vedere [Best Practices for WOW64 on](https://www.microsoft.com/whdc/system/platform/64bit/WoW64_bestprac.mspx) Windows Hardware Developer Central (Procedure consigliate per WOW64 in Windows Hardware Developer Central).

### <a name="potential-compatibility-pitfalls"></a>Potenziali problemi di compatibilità

La maggior parte delle applicazioni sviluppate per una piattaforma a 32 bit verrà eseguita senza problemi in una piattaforma a 64 bit. Alcune applicazioni potrebbero avere problemi, tra cui i seguenti:

-   Tutti i driver per le edizioni a 64 bit Windows sistemi operativi devono essere versioni a 64 bit. La richiesta di nuovi driver a 64 bit ha implicazioni per gli schemi di protezione della copia che si basano su driver meno recenti. Si noti che i driver in modalità kernel devono essere firmati con Authenticode per essere caricati da edizioni a 64 bit di Windows.
-   I processi a 64 bit non possono caricare DLL a 32 bit e i processi a 32 bit non possono caricare DLL a 64 bit. Gli sviluppatori devono assicurarsi che le versioni a 64 bit delle DLL di terze parti siano disponibili prima di procedere con lo sviluppo. Se è necessario usare una DLL a 32 bit in un processo a 64 bit, è possibile Windows la comunicazione tra processi (IPC). I componenti COM possono anche usare i server out-of-process e il marshalling per comunicare tra i limiti, ma questa operazione può causare una penalizzazione delle prestazioni.
-   Molti processori x64 sono anche processori multi-core e gli sviluppatori devono testare in che modo questo influisce sulle applicazioni legacy. Altre informazioni sui processori multicore e sulle implicazioni per le applicazioni di gioco sono disponibili in Tempo di gioco [e processori multicore.](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)
-   Le applicazioni devono anche chiamare [**SHGetFolderPath per**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) individuare i percorsi dei file, perché in alcuni casi alcuni nomi di cartella sono cambiati. Ad esempio, CSIDL PROGRAM FILES restituirebbe \_ \_ "C: Programmi(x86)" per un'applicazione a 32 bit in esecuzione su una piattaforma \\ a 64 bit anziché "C: \\ Programmi". Gli sviluppatori devono tenere presente il funzionamento delle funzionalità di reindirizzamento e reflection dell'emulatore WOW64.

Inoltre, gli sviluppatori devono fare diffidare dei programmi a 16 bit che potrebbero essere ancora in uso. WOW64 non è in grado di gestire applicazioni a 16 bit. sono inclusi i programmi di installazione e tutti i programmi MS-DOS.

> [!Note]  
> I problemi di compatibilità più comuni sono i programmi di installazione che eseguono codice a 16 bit e non hanno driver a 64 bit per gli schemi di protezione della copia.

 

La sezione successiva illustra i problemi relativi alla portabilità del codice nativo a 64 bit per gli sviluppatori che vogliono garantire il funzionamento dei programmi legacy su piattaforme a 64 bit. È anche per gli sviluppatori che non hanno familiarità con la programmazione a 64 bit.

## <a name="porting-applications-to-64-bit-platforms"></a>Porting di applicazioni su piattaforme a 64 bit

La presenza degli strumenti e delle librerie più utili consente di semplificare la transizione dallo sviluppo a 32 bit a quello a 64 bit. DirectX 9 SDK include librerie per supportare progetti basati su x86 e x64. Microsoft Visual Studio 2005 e Visual Studio 2008 supportano la generazione di codice per x86 e x64 e sono dotate di librerie ottimizzate per la generazione di codice x64. Tuttavia, sarà anche necessario per gli sviluppatori distribuire i runtime di Visual C con le proprie applicazioni. Si noti che le edizioni Express di Visual Studio 2005 e Visual Studio 2008 non includono il compilatore x64, ma tutte le edizioni Standard, Professional e Team System.

Gli sviluppatori che hanno come destinazione piattaforme a 32 bit possono preparare lo sviluppo a 64 bit per semplificare la transizione in un secondo momento. Durante la compilazione di progetti a 32 bit, gli sviluppatori devono usare il flag /Wp64, che causerà la generazione di avvisi relativi a problemi che influiscono sulla portabilità. Il passaggio a librerie e strumenti a 64 bit genererà inizialmente molti nuovi errori di compilazione. Pertanto, è consigliabile cambiare strumenti e librerie indipendenti dai bit e correggere eventuali avvisi prima di passare a una compilazione a 64 bit.

La modifica degli strumenti, la modifica delle librerie e l'uso di determinati flag del compilatore non saranno tuttavia sufficienti. I presupposti negli standard di codifica devono essere rivalutati per garantire che gli standard di codifica correnti non consentano problemi di portabilità. I problemi di portabilità possono includere il troncamento del puntatore, le dimensioni e l'allineamento dei tipi di dati, la responsabilità delle DLL a 32 bit, l'uso di API legacy, il codice assembly e i vecchi file binari.

> [!Note]  
> Visual C++ 2010 include le intestazioni stdint.h e cstdint C99 che definiscono i tipi di portabilità standard int32 \_ t, uint32 \_ t, int64 \_ t, uint64 \_ t, intptr \_ t e uintptr \_ t. L'uso di questi tipi insieme ai tipi di dati standard ptrdiff t e size t può essere preferibile ai tipi di portabilità Windows usati di seguito per migliorare la portabilità \_ \_ del codice.

 

Di seguito sono riportati i principali problemi di portabilità:

<dl> <dt>

<span id="Pointer_Truncation"></span><span id="pointer_truncation"></span><span id="POINTER_TRUNCATION"></span>**Troncamento del puntatore**
</dt> <dd>

I puntatori sono a 64 bit in un sistema operativo a 64 bit, quindi il cast dei puntatori ad altri tipi di dati può comportare il troncamento e l'aritmetica dei puntatori può causare il danneggiamento. L'uso del flag /Wp64 genererà un avviso su questo tipo di problema, ma l'uso di tipi polimorfici (INT \_ PTR, DWORD \_ PTR, SIZE \_ T, UINT PTR e così via) quando si esegue il cast dei tipi di puntatore è una procedura consigliata per evitare completamente questo \_ problema. Poiché i puntatori sono a 64 bit nelle nuove piattaforme, gli sviluppatori devono controllare l'ordine dei puntatori e i tipi di dati nelle classi e nelle strutture, per ridurre o eliminare la spaziatura interna.

</dd> <dt>

<span id="Data_Types_and_Binary_Files"></span><span id="data_types_and_binary_files"></span><span id="DATA_TYPES_AND_BINARY_FILES"></span>**Tipi di dati e file binari**
</dt> <dd>

Mentre i puntatori aumentano da 32 bit a 64 in una piattaforma a 64 bit, altri tipi di dati no. I tipi di dati a precisione fissa (DWORD32, DWORD64, INT32, INT64, LONG32, LONG64, UINT32, UINT64) possono essere usati in posizioni in cui è necessario conoscere le dimensioni del tipo di dati; ad esempio in una struttura di file binaria. Le modifiche apportate alle dimensioni del puntatore e all'allineamento dei dati richiedono una gestione speciale per garantire la compatibilità da 32 bit a 64 bit. Altre informazioni sono disponibili in [Getting Ready for 64-bit Windows: The New Data Types](/windows/desktop/WinProg64/the-new-data-types).

</dd> <dt>

<span id="Older_Win32_APIs_and_Data_Alignment"></span><span id="older_win32_apis_and_data_alignment"></span><span id="OLDER_WIN32_APIS_AND_DATA_ALIGNMENT"></span>**API Win32 precedenti e allineamento dei dati**
</dt> <dd>

Alcune API Win32 sono state deprecate e sostituite con chiamate API più neutre, ad esempio SetWindowLongPtr al posto di SetWindowLong.

La penalità delle prestazioni per gli accessi non allineati è maggiore nella piattaforma x64 che in una piattaforma x86. Le macro TYPE \_ ALIGNMENT(t) e FIELD OFFSET(t, member) possono essere usate per determinare le informazioni di allineamento che possono essere \_ usate direttamente dal codice. L'uso corretto di queste macro citate dovrebbe eliminare potenziali penalità per l'accesso non allineato.

Altre informazioni sulla macro TYPE ALIGNMENT, sulla macro FIELD OFFSET e sulla programmazione generale a 64 bit sono disponibili in Programmazione \_ \_ di Windows a [64 bit: Migration Suggerimenti: Additional Considerations](/windows/desktop/WinProg64/additional-considerations) and Getting Ready for [64-bit Windows: Rules for Using Pointers](/windows/desktop/WinProg64/rules-for-using-pointers).

</dd> <dt>

<span id="Assembly_Code"></span><span id="assembly_code"></span><span id="ASSEMBLY_CODE"></span>**Codice assembly**
</dt> <dd>

Il codice assembly inline non è supportato nelle piattaforme a 64 bit e deve essere sostituito. Le modifiche all'architettura possono aver modificato i colli di bottiglia dell'applicazione e C/C++ o oggetti intrinseci possono ottenere risultati simili con codice più facile da leggere. La procedura più consigliabile consiste nel passare tutto il codice assembly a C o C++. Le funzioni intrinseche possono essere usate al posto del codice assembly, ma devono essere usate solo dopo l'esecuzione della profilatura e dell'analisi complete.

X87, MMX e 3DNow! I set di istruzioni sono deprecati nelle modalità a 64 bit. I set di istruzioni sono ancora presenti per la compatibilità con le versioni precedenti per la modalità a 32 bit. Tuttavia, per evitare problemi di compatibilità in futuro, è sconsigliato il loro uso nei progetti correnti e futuri.

</dd> <dt>

<span id="Deprecated_APIs"></span><span id="deprecated_apis"></span><span id="DEPRECATED_APIS"></span>**API deprecate**
</dt> <dd>

Alcune API DirectX meno recenti sono state eliminate per le applicazioni native a 64 bit: DirectPlay 4 e versioni precedenti, DirectDraw 6 e versioni precedenti, Direct3D 8 e versioni precedenti e DirectInput 7 e versioni precedenti. Inoltre, l'API di base di DirectMusic è disponibile per le applicazioni native a 64 bit, ma il livello prestazioni e DirectMusic Producer sono deprecati.

Visual Studio avvisi di deprecazione e queste modifiche non sono un problema per gli sviluppatori che usano le API più recenti.

</dd> </dl>

## <a name="profiling-and-optimization-of-ported-applications"></a>Profilatura e ottimizzazione delle applicazioni portate

Tutti gli sviluppatori devono profilare di nuovo tutte le applicazioni da convertire in nuove architetture. Molte applicazioni da convertire in piattaforme a 64 bit avranno profili di prestazioni diversi rispetto alle versioni a 32 bit. Gli sviluppatori devono eseguire test delle prestazioni a 64 bit prima di valutare gli elementi da ottimizzare. La buona notizia è che molte ottimizzazioni tradizionali funzionano su piattaforme a 64 bit. Inoltre, i compilatori a 64 bit possono anche eseguire molte ottimizzazioni con l'uso corretto di flag del compilatore e hint di codifica.

Alcuni tipi di dati interni di alcune strutture possono essere riordinati per risparmiare spazio di memoria e migliorare la memorizzazione nella cache. In alcuni casi è possibile usare indici di matrice anziché un puntatore completo a 64 bit. Il flag /fp:fast può migliorare l'ottimizzazione e la vettorizzazione a virgola mobile. \_ \_ L'uso di restrict, declspec(restrict) e declspec(noalias) consente al compilatore di risolvere gli alias e migliorare l'uso del file di registro.

Altre informazioni su /fp:fast sono disponibili in [/fp (Specifica Floating-Point comportamento).](/cpp/build/reference/fp-specify-floating-point-behavior)

Per altre informazioni \_ \_ su restrict, vedere [Modificatori specifici di Microsoft.](/cpp/cpp/microsoft-specific-modifiers)

Altre informazioni su declspec(restrict) sono disponibili in [Procedure consigliate per l'ottimizzazione.](/cpp/build/optimization-best-practices)

Altre informazioni su declspec(noalias) sono disponibili in [ \_ \_ declspec(noalias).](https://msdn.microsoft.com/library/k649tyc7(VS.80).aspx)

## <a name="managed-code-on-a-64-bit-operating-system"></a>Codice gestito in un sistema operativo a 64 bit

Il codice gestito viene usato da molti sviluppatori di giochi nella catena di strumenti, quindi può essere utile comprendere il comportamento in un sistema operativo a 64 bit. Il codice gestito è indipendente dal set di istruzioni, pertanto quando si esegue un'applicazione gestita in un sistema operativo a 64 bit, Common Language Runtime (CLR) può eseguirla come processo a 32 bit o a 64 bit. Per impostazione predefinita, CLR esegue le applicazioni gestite a 64 bit e dovrebbero funzionare correttamente senza problemi. Tuttavia, se l'applicazione dipende da una DLL nativa a 32 bit, l'applicazione avrà esito negativo quando tenta di chiamare questa DLL. Un processo a 64 bit richiede codice completamente a 64 bit e non è possibile chiamare una DLL a 32 bit da un processo a 64 bit. La soluzione migliore a lungo termine consiste nel compilare il codice nativo anche a 64 bit, ma una soluzione a breve termine perfettamente ragionevole consiste nel contrassegnare semplicemente l'applicazione gestita come per x86 solo usando il flag di compilazione /platform:x86.

## <a name="performance-implications-of-running-a-64-bit-operating-system"></a>Implicazioni relative alle prestazioni dell'esecuzione di un sistema operativo a 64 bit

Poiché i processori con architettura AMD64 e Intel 64 possono eseguire istruzioni a 32 bit in modo nativo, possono eseguire applicazioni a 32 bit alla massima velocità, anche in un sistema operativo a 64 bit. La conversione dei parametri tra 32 bit e 64 bit quando si chiamano le funzioni del sistema operativo ha un costo moderio, ma questo costo è in genere trascurabile. Ciò significa che non dovrebbe verificarsi alcun rallentamento durante l'esecuzione di applicazioni a 32 bit in un sistema operativo a 64 bit.

Quando si compilano applicazioni a 64 bit, i calcoli si complicano. Un programma a 64 bit usa puntatori a 64 bit e le relative istruzioni sono leggermente più grandi, quindi il requisito di memoria è leggermente aumentato. Ciò può causare un leggero calo delle prestazioni. D'altra parte, la presenza di un numero doppio di registri e la possibilità di eseguire calcoli di interi a 64 bit in una singola istruzione saranno spesso più che compensate. Il risultato finale è che un'applicazione a 64 bit potrebbe essere eseguita leggermente più lentamente rispetto alla stessa applicazione compilata a 32 bit, ma spesso verrà eseguita leggermente più velocemente.

## <a name="summary"></a>Riepilogo

Le architetture a 64 bit consentono agli sviluppatori di eseguire il push delle limitazioni relative all'aspetto, al suono e al gioco dei giochi. La transizione dalla programmazione a 32 bit alla programmazione a 64 bit non è tuttavia semplice. Comprendendo le differenze tra i due strumenti e usando gli strumenti più recenti, la transizione alle piattaforme a 64 bit può essere più semplice e veloce.

Altre informazioni sulla programmazione a 64 bit sono disponibili in [Visual C++ Developer Center: 64-Bit Programming](https://msdn.microsoft.com/vstudio//aa336463.aspx)( Centro per sviluppatori: Programmazione a 64 bit).

 

 