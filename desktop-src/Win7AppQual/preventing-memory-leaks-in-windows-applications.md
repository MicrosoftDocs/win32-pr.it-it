---
description: Informazioni su come evitare perdite di memoria nelle Windows per le Windows 7 e Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Prevenzione delle perdite di memoria nelle Windows applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef336c52ff4869ae9947b898e8a42c480be58054315de0180ec6a18f8c917f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994797"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Prevenzione delle perdite di memoria nelle Windows applicazioni

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  

## <a name="description"></a>Descrizione

Le perdite di memoria sono una classe di bug in cui l'applicazione non riesce a rilasciare memoria quando non è più necessaria. Nel corso del tempo, le perdite di memoria influiscono sulle prestazioni sia dell'applicazione specifica che del sistema operativo. Una perdita di grandi dimensioni potrebbe comportare tempi di risposta inaccettabili a causa di un paging eccessivo. Alla fine si verificano errori nell'applicazione e in altre parti del sistema operativo.

Windows libera tutta la memoria allocata dall'applicazione al termine del processo, pertanto le applicazioni con esecuzione breve non influiranno in modo significativo sulle prestazioni complessive del sistema. Tuttavia, le perdite nei processi a esecuzione lunga, ad esempio i servizi o anche i plug-in explorer, possono influire notevolmente sull'affidabilità del sistema e potrebbero forzare l'utente a riavviare Windows per rendere nuovamente utilizzabile il sistema.

Le applicazioni possono allocare memoria per loro conto in più mezzi. Ogni tipo di allocazione può comportare una perdita se non viene liberata dopo l'utilizzo. Ecco alcuni esempi di modelli di allocazione comuni:

-   Memoria heap tramite la [**funzione HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) o i relativi equivalenti di runtime C/C++ **malloc** o **new**
-   Allocazioni dirette dal sistema operativo tramite la [**funzione VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   Gli handle del kernel creati tramite API Kernel32, ad esempio [**CreateFile,**](/windows/win32/api/fileapi/nf-fileapi-createfilea) [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)o [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)mantendono la memoria del kernel per conto dell'applicazione
-   Handle GDI e USER creati tramite le API User32 e Gdi32 (per impostazione predefinita, ogni processo ha una quota di 10.000 handle)

## <a name="best-practices"></a>Procedure consigliate

Il monitoraggio dell'utilizzo delle risorse dell'applicazione nel tempo è il primo passaggio per rilevare e diagnosticare le perdite di memoria. Usare Windows Gestione attività e aggiungere le colonne seguenti: "Commit Size", "Handles", "User Objects" e "GDI Objects". In questo modo sarà possibile stabilire una baseline per l'applicazione e monitorare l'utilizzo delle risorse nel tempo.

![Screenshot che mostra la pagina "Processi" in Windows Gestione attività.](images/preventingmemoryleaks-windowstaskmanager.gif)

Gli strumenti Microsoft seguenti forniscono informazioni più dettagliate e consentono di rilevare e diagnosticare le perdite per i vari tipi di allocazione nell'applicazione:

-   Monitor prestazioni e Monitoraggio risorse fanno parte di Windows 7 e possono monitorare e grafire l'uso delle risorse nel tempo
-   La versione più recente di Application Verifier diagnosticare perdite di heap in Windows 7
-   UMDH, che fa parte degli strumenti di debug per Windows, analizza le allocazioni di memoria heap per un determinato processo e può aiutare a trovare perdite e altri modelli di utilizzo insoliti
-   Xperf è uno strumento di analisi delle prestazioni sofisticato con supporto per le tracce di allocazione heap
-   L'heap di debug CRT tiene traccia delle allocazioni di heap e consente di creare funzionalità di debug dell'heap

Alcune procedure di codifica e progettazione possono limitare il numero di perdite nel codice.

-   Usare puntatori intelligenti nel codice C++ sia per le allocazioni di heap che per le risorse Win32 come **handle del** kernel. La libreria standard C++ fornisce la **classe \_ ptr automatica per** le allocazioni di heap. Per altri tipi di allocazione è necessario scrivere classi personalizzate. La libreria ATL fornisce un set di classi per la gestione automatica delle risorse per gli oggetti heap e gli handle del kernel
-   Usare funzionalità intrinseche del compilatore come **\_ com \_ ptr \_ t** per incapsulare i puntatori a interfaccia COM in "puntatori intelligenti" e facilitare il conteggio dei riferimenti. Esistono classi simili per altri tipi di dati COM: **\_ bstr \_ t** e **\_ variant \_ t**
-   Monitorare l'utilizzo insolito di memoria del codice .NET. Il codice gestito non è immune alle perdite di memoria. Per [informazioni su come individuare le perdite gc,](/archive/blogs/ricom/) vedere "Rilevamento delle perdite di memoria managed memory"
-   Tenere presente i modelli di perdita nel codice lato client Web. I riferimenti circolari tra oggetti COM e motori di scripting come JScript possono causare perdite di grandi dimensioni nelle applicazioni Web. ["Understanding and Solving Internet Explorer Leak Patterns"](/previous-versions/ms976398(v=msdn.10)) (Informazioni e risoluzione dei Internet Explorer di perdite di dati) contiene altre informazioni su questi tipi di perdite. È possibile usare Rilevamento perdite di memoria JavaScript per eseguire il debug delle perdite di memoria nel codice. Anche se Windows Internet Explorer 8, che viene Windows 7, riduce la maggior parte di questi problemi, i browser meno recenti sono ancora vulnerabili a questi bug
-   Evitare di usare più percorsi di uscita da una funzione. Le allocazioni assegnate alle variabili nell'ambito della funzione devono essere liberate in un blocco specifico alla fine della funzione
-   Non usare eccezioni nel codice senza liberare tutte le variabili locali nelle funzioni. Se si usano eccezioni native, liberare tutte le allocazioni all'interno \_ \_ del blocco finally. Se si usano eccezioni C++, è necessario eseguire il wrapping di tutte le allocazioni di heap e handle in puntatori intelligenti
-   Non eliminare o reinizializzare [**un oggetto PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) senza chiamare la [**funzione PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Collegamenti alle risorse

*Modelli di allocazione comuni:*

-   [**Funzione di allocazione heap**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Funzione di allocazione della memoria**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**Operatore New (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Funzione di allocazione virtuale**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Oggetti kernel](../sysinfo/kernel-objects.md)
-   [Handle di oggetto GDI](../sysinfo/gdi-objects.md)
-   [Interfaccia utente handle di oggetto](../sysinfo/user-objects.md)

*Strumenti Microsoft:*

-   [Application Verifier](application-verifier.md)
-   [Strumenti di debug per Windows](/windows-hardware/drivers/debugger/)
-   [Heap dump modalità utente](/windows-hardware/drivers/debugger/umdh)
-   [Strumento di acquisizione, elaborazione e analisi delle tracce](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [CRT Debug Heap](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Collegamenti aggiuntivi:*

-   [**Classe \_ auto ptr**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [classi Active Template Library (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_Oggetto com \_ ptr \_ t**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_Classe bstr \_ t**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_Classe variant \_ yt**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Tracking down managed memory leaks"](/archive/blogs/ricom/)
-   ["Understanding and Solving Internet Explorer Leak Patterns"](/previous-versions/ms976398(v=msdn.10))
-   ["Rilevamento perdite di memoria JavaScript"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Mitigazione della perdita di memoria circolare (nei browser):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**Istruzione try-finally**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**Struttura PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**Funzione PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
