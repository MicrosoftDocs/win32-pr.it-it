---
description: Informazioni su come prevenire le perdite di memoria nelle applicazioni Windows per le piattaforme Windows 7 e Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Prevenzione delle perdite di memoria nelle applicazioni Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "104554618"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Prevenzione delle perdite di memoria nelle applicazioni Windows

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  

## <a name="description"></a>Descrizione

Le perdite di memoria sono una classe di bug in cui l'applicazione non riesce a rilasciare la memoria quando non è più necessaria. Nel tempo le perdite di memoria influiscono sulle prestazioni dell'applicazione specifica e del sistema operativo. Una perdita di grandi dimensioni può causare tempi di risposta inaccettabili a causa di un paging eccessivo. Infine, l'applicazione e altre parti del sistema operativo si verificheranno errori.

Windows consente di liberare tutta la memoria allocata dall'applicazione alla chiusura del processo, quindi le applicazioni a esecuzione prolungata non influiscono significativamente sulle prestazioni complessive del sistema. Tuttavia, le perdite nei processi a esecuzione prolungata come i servizi o anche i plug-in di Esplora risorse possono avere un notevole effetto sull'affidabilità del sistema e possono forzare l'utente a riavviare Windows per riutilizzarlo di nuovo.

Le applicazioni possono allocare memoria per conto di più mezzi. Ogni tipo di allocazione può causare una perdita se non viene liberato dopo l'utilizzo. Di seguito sono riportati alcuni esempi di modelli di allocazione comuni:

-   Memoria heap tramite la funzione [**HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) o i relativi equivalenti di runtime C/C++ **malloc** o **New**
-   Allocazioni dirette dal sistema operativo tramite la funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .
-   Gli handle del kernel creati tramite le API Kernel32 come [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea), [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)o [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)contengono memoria kernel per conto dell'applicazione
-   GDI e handle utente creati tramite le API User32 e gdi32 (per impostazione predefinita, ogni processo ha una quota di 10.000 handle)

## <a name="best-practices"></a>Procedure consigliate

Il monitoraggio del consumo di risorse dell'applicazione nel corso del tempo è il primo passaggio per rilevare e diagnosticare le perdite di memoria. Utilizzare Gestione attività di Windows e aggiungere le colonne seguenti: "dimensioni commit", "handle", "oggetti utente" e "oggetti GDI". Ciò consentirà di stabilire una linea di base per l'applicazione e di monitorare l'utilizzo delle risorse nel tempo.

![Screenshot che mostra la pagina "processi" in Gestione attività di Windows.](images/preventingmemoryleaks-windowstaskmanager.gif)

Gli strumenti Microsoft seguenti forniscono informazioni più dettagliate e possono aiutare a rilevare e diagnosticare le perdite per i vari tipi di allocazione nell'applicazione:

-   Performance Monitor e Monitoraggio risorse fanno parte di Windows 7 e possono monitorare e tracciare l'utilizzo delle risorse nel tempo
-   La versione più recente di Application Verifier è in grado di diagnosticare le perdite di heap in Windows 7
-   UMDH, che fa parte degli strumenti di debug per Windows, analizza le allocazioni di memoria heap per un determinato processo e può aiutare a individuare le perdite e altri modelli di utilizzo insoliti
-   Xperf è uno strumento di analisi delle prestazioni sofisticato con supporto per le tracce di allocazione heap
-   L'heap di debug CRT tiene traccia delle allocazioni di heap e consente di compilare le funzionalità di debug dell'heap

Alcune procedure di codifica e progettazione possono limitare il numero di perdite nel codice.

-   Usare i puntatori intelligenti nel codice C++ per le allocazioni di heap e per le risorse Win32, ad esempio gli **handle** del kernel. La libreria standard C++ fornisce la **classe \_ ptr automatica** per le allocazioni di heap. Per altri tipi di allocazione sarà necessario scrivere classi personalizzate. La libreria ATL offre un set completo di classi per la gestione automatica delle risorse sia per gli oggetti heap che per gli handle del kernel
-   Usare le funzionalità intrinseche del compilatore, come **\_ com \_ ptr \_ t** , per incapsulare i puntatori dell'interfaccia com in "puntatori intelligenti" e supportare il conteggio dei riferimenti. Esistono classi simili per altri tipi di dati COM: **\_ BSTR \_ t** e **\_ Variant \_ t**
-   Monitorare l'utilizzo insolito della memoria per il codice .NET. Il codice gestito non è immune alle perdite di memoria. Vedere ["rilevamento delle perdite di managed memory"](/archive/blogs/ricom/) per informazioni su come trovare le perdite GC
-   Tenere presente i modelli di perdita nel codice sul lato client Web. I riferimenti circolari tra oggetti COM e motori di script come JScript possono causare perdite di grandi dimensioni nelle applicazioni Web. ["Comprensione e risoluzione dei modelli di perdita di Internet Explorer"](/previous-versions/ms976398(v=msdn.10)) contiene altre informazioni su questi tipi di perdite. Per eseguire il debug di perdite di memoria nel codice, è possibile usare il rilevatore di perdite di memoria JavaScript. Sebbene Windows Internet Explorer 8, fornito con Windows 7, rilevi la maggior parte di questi problemi, i browser meno recenti sono ancora vulnerabili a questi bug
-   Evitare di usare più percorsi di uscita da una funzione. Le allocazioni assegnate a variabili nell'ambito della funzione devono essere liberate in un blocco particolare alla fine della funzione
-   Non usare eccezioni nel codice senza liberare tutte le variabili locali nelle funzioni. Se si utilizzano eccezioni native, liberare tutte le allocazioni all'interno del \_ \_ blocco finally. Se si usano le eccezioni C++, è necessario che tutte le allocazioni di heap e handle siano racchiuse nei puntatori intelligenti
-   Non rimuovere o reinizializzare un oggetto [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) senza chiamare la funzione [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Collegamenti alle risorse

*Modelli di allocazione comuni:*

-   [**Funzione di allocazione heap**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Funzione di allocazione della memoria**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**Operatore New (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Funzione di allocazione virtuale**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Oggetti kernel](../sysinfo/kernel-objects.md)
-   [Handle di oggetti GDI](../sysinfo/gdi-objects.md)
-   [Handle oggetto interfaccia utente](../sysinfo/user-objects.md)

*Strumenti Microsoft:*

-   [Application Verifier](application-verifier.md)
-   [Strumenti di debug per Windows](/windows-hardware/drivers/debugger/)
-   [Heap dump in modalità utente](/windows-hardware/drivers/debugger/umdh)
-   [Strumento di acquisizione, elaborazione e analisi delle tracce](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [Heap di debug CRT](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Collegamenti aggiuntivi:*

-   [**\_classe PTR automatico**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Classi di memoria Active Template Library (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_\_oggetto com PTR \_ t**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_\_classe BSTR t**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_Classe della variante \_ YT**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Rilevamento delle perdite di managed memory"](/archive/blogs/ricom/)
-   ["Comprensione e risoluzione dei modelli di perdita di Internet Explorer"](/previous-versions/ms976398(v=msdn.10))
-   ["Rilevatore di perdite di memoria JavaScript"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Attenuazione della perdita di memoria circolare (nei browser):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**Istruzione try-finally**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**Struttura PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**PropVariantClear (funzione)**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
