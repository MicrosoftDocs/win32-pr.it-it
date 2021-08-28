---
title: Annotazioni di intestazione
description: Le annotazioni di intestazione descrivono come una funzione usa i parametri e il valore restituito.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows API, annotazioni del file di intestazione
- annotazioni del file di intestazione
- Specstrings.h
- standard annotation language (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ad560d00c45714d0feaa9ab2fa58ff4c985730fd563d4943ff028f561f2793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643631"
---
# <a name="header-annotations"></a>Annotazioni di intestazione

\[Questo argomento descrive le annotazioni supportate nelle intestazioni Windows tramite Windows 7. Se si sviluppa per Windows 8, è consigliabile usare le annotazioni descritte in [Annotazioni SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]

Le annotazioni di intestazione descrivono come una funzione usa i parametri e il valore restituito. Queste annotazioni sono state aggiunte a molti dei Windows di intestazione per assicurarsi di chiamare correttamente l'API Windows. Se si abilita l'analisi del codice, disponibile a partire da Visual Studio 2005, il compilatore genererà avvisi di livello 6000 se non si chiamano queste funzioni in base all'utilizzo descritto tramite le annotazioni. È anche possibile aggiungere queste annotazioni nel codice per assicurarsi che vengano chiamate correttamente. Per abilitare l'analisi del codice Visual Studio, vedere la documentazione per la versione di Visual Studio.

Queste annotazioni sono definite in Specstrings.h. Sono compilate su primitive che fanno parte del linguaggio SAL (Standard Annotation Language) e implementate tramite `_declspec("SAL_*")` .

Esistono due classi di annotazioni: annotazioni del buffer e annotazioni avanzate.

## <a name="buffer-annotations"></a>Annotazioni del buffer

Le annotazioni del buffer descrivono come le funzioni usano i puntatori e possono essere usate per rilevare i sovraccarichi del buffer. Ogni parametro può usare zero o un'annotazione del buffer. Un'annotazione del buffer viene costruita con un carattere di sottolineatura iniziale e i componenti descritti nelle sezioni seguenti.



| Dimensioni del buffer                                                                                  | Descrizione                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*size*)<br/>                        | Specifica le dimensioni totali del buffer. Usare con \_ bcount ed \_ ecount. Non usare con \_ part. Questo valore è lo spazio accessibile. può essere minore dello spazio allocato.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)<br/> | Specifica le dimensioni totali e la lunghezza inizializzata del buffer. Usare con \_ la parte bcount \_ e la \_ parte \_ ecount. Le dimensioni totali possono essere inferiori allo spazio allocato.<br/>              |



 



| Unità di dimensione del buffer                                                       | Descrizione                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | Le dimensioni del buffer sono in byte.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | Le dimensioni del buffer sono in elementi.<br/> |



 



| Direzione                                                            | Descrizione                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_Pollici<br/>          | La funzione legge dal buffer. Il chiamante fornisce il buffer e lo inizializza.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_Inout<br/> | La funzione legge da e scrive nel buffer. Il chiamante fornisce il buffer e lo inizializza. Se usato con \_ deref, il buffer può essere riallocato dalla funzione .<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_Cambio<br/>       | La funzione scrive nel buffer. Se usata sul valore restituito o con \_ deref, la funzione fornisce il buffer e lo inizializza. In caso contrario, il chiamante fornisce il buffer e la funzione lo inizializza.<br/> |



 



| Riferimento indiretto                                                                       | Descrizione                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_deref<br/>              | Dereferenziare il parametro per ottenere il puntatore al buffer. Questo parametro non può essere **NULL.**<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref \_ opt<br/> | Dereferenziare il parametro per ottenere il puntatore al buffer. Questo parametro può essere **NULL**.<br/>     |



 



| Inizializzazione                                                    | Descrizione                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_Completo<br/> | La funzione inizializza l'intero buffer. Usare solo con i buffer di output.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_Parte<br/> | La funzione inizializza parte del buffer e indica in modo esplicito la quantità. Usare solo con i buffer di output.<br/> |



 



| Buffer obbligatorio o facoltativo                                    | Descrizione                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_Optare<br/> | Questo parametro può essere **NULL**.<br/> |



 

L'esempio seguente illustra le annotazioni per la **funzione GetModuleFileName.** Il *parametro hModule* è un parametro di input facoltativo. Il *parametro lpFilename* è un parametro di output. la dimensione in caratteri è specificata dal *parametro nSize* e la relativa lunghezza include il carattere di terminazione **Null.** Il *parametro nSize* è un parametro di input.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



Di seguito sono riportate le annotazioni definite in Specstrings.h. Usare le informazioni nelle tabelle precedenti per interpretarne il significato.

__bcount(*size*)  
__bcount_opt(*size*)  
__deref_bcount(*size*)  
__deref_bcount_opt(*size*)  
__deref_ecount(*size*)  
__deref_ecount_opt(*size*)  
__deref_in  
__deref_in_bcount(*size*)  
__deref_in_bcount_opt(*size*)  
__deref_in_ecount(*size*)  
__deref_in_ecount_opt(*size*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount(*size*)  
__deref_inout_bcount_full(*size*)  
__deref_inout_bcount_full_opt(*size*)  
__deref_inout_bcount_opt(*size*)  
__deref_inout_bcount_part(*size*,*length*)  
__deref_inout_bcount_part_opt(*size*,*length*)  
__deref_inout_ecount(*size*)  
__deref_inout_ecount_full(*size*)  
__deref_inout_ecount_full_opt(*size*)  
__deref_inout_ecount_opt(*size*)  
__deref_inout_ecount_part(*size*,*length*)  
__deref_inout_ecount_part_opt(*size*,*length*)  
__deref_inout_opt  
__deref_opt_bcount(*size*)  
__deref_opt_bcount_opt(*size*)  
__deref_opt_ecount(*size*)  
__deref_opt_ecount_opt(*size*)  
__deref_opt_in  
__deref_opt_in_bcount(*size*)  
__deref_opt_in_bcount_opt(*size*)  
__deref_opt_in_ecount(*size*)  
__deref_opt_in_ecount_opt(*size*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount(*size*)  
__deref_opt_inout_bcount_full(*size*)  
__deref_opt_inout_bcount_full_opt(*size*)  
__deref_opt_inout_bcount_opt(*size*)  
__deref_opt_inout_bcount_part(*size*,*length*)  
__deref_opt_inout_bcount_part_opt(*size*,*length*)  
__deref_opt_inout_ecount(*size*)  
__deref_opt_inout_ecount_full(*size*)  
__deref_opt_inout_ecount_full_opt(*size*)  
__deref_opt_inout_ecount_opt(*size*)  
__deref_opt_inout_ecount_part(*size*,*length*)  
__deref_opt_inout_ecount_part_opt(*size*,*length*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount(*size*)  
__deref_opt_out_bcount_full(*size*)  
__deref_opt_out_bcount_full_opt(*size*)  
__deref_opt_out_bcount_opt(*size*)  
__deref_opt_out_bcount_part(*size*,*length*)  
__deref_opt_out_bcount_part_opt(*size*,*length*)  
__deref_opt_out_ecount(*size*)  
__deref_opt_out_ecount_full(*size*)  
__deref_opt_out_ecount_full_opt(*size*)  
__deref_opt_out_ecount_opt(*size*)  
__deref_opt_out_ecount_part(*size*,*length*)  
__deref_opt_out_ecount_part_opt(*size*,*length*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount(*size*)  
__deref_out_bcount_full(*size*)  
__deref_out_bcount_full_opt(*size*)  
__deref_out_bcount_opt(*size*)  
__deref_out_bcount_part(*size*,*length*)  
__deref_out_bcount_part_opt(*size*,*length*)  
__deref_out_ecount(*size*)  
__deref_out_ecount_full(*size*)  
__deref_out_ecount_full_opt(*size*)  
__deref_out_ecount_opt(*size*)  
__deref_out_ecount_part(*size*,*length*)  
__deref_out_ecount_part_opt(*size*,*length*)  
__deref_out_opt  
__ecount(*size*)  
__ecount_opt(*size*)  
__in  
__in_bcount(*size*)  
__in_bcount_opt(*size*)  
__in_ecount(*size*)  
__in_ecount_opt(*size*)  
__in_opt  
__inout  
__inout_bcount(*size*)  
__inout_bcount_full(*size*)  
__inout_bcount_full_opt(*size*)  
__inout_bcount_opt(*size*)  
__inout_bcount_part(*size*,*length*)  
__inout_bcount_part_opt(*size*,*length*)  
__inout_ecount(*size*)  
__inout_ecount_full(*size*)  
__inout_ecount_full_opt(*size*)  
__inout_ecount_opt(*size*)  
__inout_ecount_part(*size*,*length*)  
__inout_ecount_part_opt(*size*,*length*)  
__inout_opt  
__out  
__out_bcount(*size*)  
__out_bcount_full(*size*)  
__out_bcount_full_opt(*size*)  
__out_bcount_opt(*size*)  
__out_bcount_part(*size*,*length*)  
__out_bcount_part_opt(*size*,*length*)  
__out_ecount(*size*)  
__out_ecount_full(*size*)  
__out_ecount_full_opt(*size*)  
__out_ecount_opt(*size*)  
__out_ecount_part(*size*,*length*)  
__out_ecount_part_opt(*size*,*length*)  
__out_opt  

## <a name="advanced-annotations"></a>Annotazioni avanzate

Le annotazioni avanzate forniscono informazioni aggiuntive sul parametro o sul valore restituito. Ogni parametro o valore restituito può usare zero o un'annotazione avanzata.



| Annotazione                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)<br/> | Le funzioni si bloccano sulla risorsa specificata.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_Callback<br/>                                                                        | La funzione può essere usata come puntatore a funzione.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | I chiamanti devono controllare il valore restituito.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_stringa di \_ formato<br/>                                                        | Il parametro è una stringa che contiene indicatori % di tipo printf.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in \_ awcount(*expr*,*size*)<br/>                            | Se l'espressione è true all'uscita, le dimensioni del buffer di input vengono specificate in byte. Se l'espressione è false, la dimensione viene specificata negli elementi .<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated<br/>                                          | È possibile accedere al buffer fino alla prima sequenza di due caratteri **Null** o puntatori.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated<br/>                                                      | È possibile accedere al buffer fino al primo carattere o puntatore **Null** incluso.<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount(*expr*,*size*)<br/>                         | Se l'espressione è true all'uscita, le dimensioni del buffer di output vengono specificate in byte. Se l'espressione è false, la dimensione viene specificata negli elementi . <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_prevalere<br/>                                                                        | Specifica il comportamento di override di tipo C# per i metodi virtuali.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_Riservati<br/>                                                                        | Il parametro è riservato per un uso futuro e deve essere zero o **NULL.**<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)<br/>                                                       | Se l'espressione è true all'uscita, il chiamante può basarsi su tutte le garanzie specificate da altre annotazioni. Se l'espressione è false, il chiamante non può basarsi sulle garanzie. Questa annotazione viene aggiunta automaticamente alle funzioni che restituiscono **un valore HRESULT.**<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)<br/>                                                    | Considerare il parametro come tipo specificato anziché come tipo dichiarato.<br/>                                                                                                                                                                                             |



 

Gli esempi seguenti illustrano il buffer e le annotazioni avanzate per le funzioni [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)e [**UnhandledExceptionFilter.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Annotazioni SAL](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[Procedura guidata: analisi del codice C/C++ per l'identificazione degli errori](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

