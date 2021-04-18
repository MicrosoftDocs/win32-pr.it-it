---
title: Annotazioni di intestazione
description: Le annotazioni di intestazione descrivono il modo in cui una funzione usa i parametri e il valore restituito.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- API Windows, annotazioni di file di intestazione
- annotazioni file di intestazione
- Specstrings. h
- linguaggio di annotazione standard (SAL)
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
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300291"
---
# <a name="header-annotations"></a>Annotazioni di intestazione

\[In questo argomento vengono descritte le annotazioni supportate nelle intestazioni di Windows tramite Windows 7. Se si sta sviluppando per Windows 8, è necessario usare le annotazioni descritte nelle [annotazioni SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]

Le annotazioni di intestazione descrivono il modo in cui una funzione usa i parametri e il valore restituito. Queste annotazioni sono state aggiunte a molti dei file di intestazione di Windows per garantire la corretta chiamata dell'API Windows. Se si Abilita l'analisi del codice, disponibile a partire da Visual Studio 2005, il compilatore produrrà avvisi di livello 6000 se non si chiamano queste funzioni in base all'utilizzo descritto tramite le annotazioni. È anche possibile aggiungere queste annotazioni nel codice per assicurarsi che venga chiamato correttamente. Per abilitare l'analisi del codice in Visual Studio, vedere la documentazione per la versione di Visual Studio in uso.

Queste annotazioni sono definite in Specstrings. h. Si basano sulle primitive che fanno parte del linguaggio di annotazione standard (SAL) e implementate tramite `_declspec("SAL_*")` .

Esistono due classi di annotazioni: le annotazioni del buffer e le annotazioni avanzate.

## <a name="buffer-annotations"></a>Annotazioni del buffer

Le annotazioni del buffer descrivono il modo in cui le funzioni utilizzano i puntatori e possono essere utilizzate per rilevare i sovraccarichi del buffer. Ogni parametro può usare un'annotazione di buffer zero o uno. Un'annotazione del buffer viene costruita con un carattere di sottolineatura principale e i componenti descritti nelle sezioni seguenti.



| Dimensioni del buffer                                                                                  | Descrizione                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_size_"></span><span id="_SIZE_"></span>(*dimensioni*)<br/>                        | Specifica la dimensione totale del buffer. Usare with \_ bcount e \_ ecount; non usare with \_ part. Questo valore è lo spazio accessibile; può essere minore dello spazio allocato.<br/> |
| <span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*dimensioni*,*lunghezza*)<br/> | Specifica la dimensione totale e la lunghezza inizializzata del buffer. Usare con la parte \_ bcount \_ e \_ ecount \_ . Le dimensioni totali possono essere inferiori allo spazio allocato.<br/>              |



 



| Unità dimensioni buffer                                                       | Descrizione                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount<br/> | Dimensioni del buffer in byte.<br/>    |
| <span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount<br/> | La dimensione del buffer è in elementi.<br/> |



 



| Direzione                                                            | Descrizione                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_in"></span><span id="_IN"></span>\_in<br/>          | La funzione legge dal buffer. Il chiamante fornisce il buffer e lo inizializza.<br/>                                                                                                                          |
| <span id="_inout"></span><span id="_INOUT"></span>\_Inout<br/> | La funzione legge e scrive nel buffer. Il chiamante fornisce il buffer e lo inizializza. Se usato con \_ Deref, il buffer può essere riallocato dalla funzione.<br/>                                      |
| <span id="_out"></span><span id="_OUT"></span>\_out<br/>       | La funzione scrive nel buffer. Se usato sul valore restituito o con \_ Deref, la funzione fornisce il buffer e lo inizializza. In caso contrario, il chiamante fornisce il buffer e la funzione la Inizializza.<br/> |



 



| Riferimento indiretto                                                                       | Descrizione                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="_deref"></span><span id="_DEREF"></span>\_Deref<br/>              | Dereferenziare il parametro per ottenere il puntatore del buffer. Questo parametro non può essere **null**.<br/> |
| <span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref \_ opt<br/> | Dereferenziare il parametro per ottenere il puntatore del buffer. Questo parametro può essere **NULL**.<br/>     |



 



| Inizializzazione                                                    | Descrizione                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="_full"></span><span id="_FULL"></span>\_completo<br/> | La funzione Inizializza l'intero buffer. Utilizzare solo con i buffer di output.<br/>                                     |
| <span id="_part"></span><span id="_PART"></span>\_parte<br/> | La funzione Inizializza parte del buffer e indica in modo esplicito la quantità. Utilizzare solo con i buffer di output.<br/> |



 



| Buffer obbligatorio o facoltativo                                    | Descrizione                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span id="_opt"></span><span id="_OPT"></span>\_consenso esplicito<br/> | Questo parametro può essere **NULL**.<br/> |



 

Nell'esempio seguente vengono illustrate le annotazioni per la funzione **GetModuleFileName** . Il parametro *hmodule* è un parametro di input facoltativo. Il parametro *lpFileName* è un parametro di output. la relativa dimensione in caratteri viene specificata dal parametro *nSize* e la relativa lunghezza include il carattere di terminazione **null**. Il parametro *nSize* è un parametro di input.


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



Di seguito sono riportate le annotazioni definite in Specstrings. h. Utilizzare le informazioni nelle tabelle precedenti per interpretarne il significato.

__bcount (*dimensioni*)  
__bcount_opt (*dimensioni*)  
__deref_bcount (*dimensioni*)  
__deref_bcount_opt (*dimensioni*)  
__deref_ecount (*dimensioni*)  
__deref_ecount_opt (*dimensioni*)  
__deref_in  
__deref_in_bcount (*dimensioni*)  
__deref_in_bcount_opt (*dimensioni*)  
__deref_in_ecount (*dimensioni*)  
__deref_in_ecount_opt (*dimensioni*)  
__deref_in_opt  
__deref_inout  
__deref_inout_bcount (*dimensioni*)  
__deref_inout_bcount_full (*dimensioni*)  
__deref_inout_bcount_full_opt (*dimensioni*)  
__deref_inout_bcount_opt (*dimensioni*)  
__deref_inout_bcount_part (*dimensioni*,*lunghezza*)  
__deref_inout_bcount_part_opt (*dimensioni*,*lunghezza*)  
__deref_inout_ecount (*dimensioni*)  
__deref_inout_ecount_full (*dimensioni*)  
__deref_inout_ecount_full_opt (*dimensioni*)  
__deref_inout_ecount_opt (*dimensioni*)  
__deref_inout_ecount_part (*dimensioni*,*lunghezza*)  
__deref_inout_ecount_part_opt (*dimensioni*,*lunghezza*)  
__deref_inout_opt  
__deref_opt_bcount (*dimensioni*)  
__deref_opt_bcount_opt (*dimensioni*)  
__deref_opt_ecount (*dimensioni*)  
__deref_opt_ecount_opt (*dimensioni*)  
__deref_opt_in  
__deref_opt_in_bcount (*dimensioni*)  
__deref_opt_in_bcount_opt (*dimensioni*)  
__deref_opt_in_ecount (*dimensioni*)  
__deref_opt_in_ecount_opt (*dimensioni*)  
__deref_opt_in_opt  
__deref_opt_inout  
__deref_opt_inout_bcount (*dimensioni*)  
__deref_opt_inout_bcount_full (*dimensioni*)  
__deref_opt_inout_bcount_full_opt (*dimensioni*)  
__deref_opt_inout_bcount_opt (*dimensioni*)  
__deref_opt_inout_bcount_part (*dimensioni*,*lunghezza*)  
__deref_opt_inout_bcount_part_opt (*dimensioni*,*lunghezza*)  
__deref_opt_inout_ecount (*dimensioni*)  
__deref_opt_inout_ecount_full (*dimensioni*)  
__deref_opt_inout_ecount_full_opt (*dimensioni*)  
__deref_opt_inout_ecount_opt (*dimensioni*)  
__deref_opt_inout_ecount_part (*dimensioni*,*lunghezza*)  
__deref_opt_inout_ecount_part_opt (*dimensioni*,*lunghezza*)  
__deref_opt_inout_opt  
__deref_opt_out  
__deref_opt_out_bcount (*dimensioni*)  
__deref_opt_out_bcount_full (*dimensioni*)  
__deref_opt_out_bcount_full_opt (*dimensioni*)  
__deref_opt_out_bcount_opt (*dimensioni*)  
__deref_opt_out_bcount_part (*dimensioni*,*lunghezza*)  
__deref_opt_out_bcount_part_opt (*dimensioni*,*lunghezza*)  
__deref_opt_out_ecount (*dimensioni*)  
__deref_opt_out_ecount_full (*dimensioni*)  
__deref_opt_out_ecount_full_opt (*dimensioni*)  
__deref_opt_out_ecount_opt (*dimensioni*)  
__deref_opt_out_ecount_part (*dimensioni*,*lunghezza*)  
__deref_opt_out_ecount_part_opt (*dimensioni*,*lunghezza*)  
__deref_opt_out_opt  
__deref_out  
__deref_out_bcount (*dimensioni*)  
__deref_out_bcount_full (*dimensioni*)  
__deref_out_bcount_full_opt (*dimensioni*)  
__deref_out_bcount_opt (*dimensioni*)  
__deref_out_bcount_part (*dimensioni*,*lunghezza*)  
__deref_out_bcount_part_opt (*dimensioni*,*lunghezza*)  
__deref_out_ecount (*dimensioni*)  
__deref_out_ecount_full (*dimensioni*)  
__deref_out_ecount_full_opt (*dimensioni*)  
__deref_out_ecount_opt (*dimensioni*)  
__deref_out_ecount_part (*dimensioni*,*lunghezza*)  
__deref_out_ecount_part_opt (*dimensioni*,*lunghezza*)  
__deref_out_opt  
__ecount (*dimensioni*)  
__ecount_opt (*dimensioni*)  
__in  
__in_bcount (*dimensioni*)  
__in_bcount_opt (*dimensioni*)  
__in_ecount (*dimensioni*)  
__in_ecount_opt (*dimensioni*)  
__in_opt  
__inout  
__inout_bcount (*dimensioni*)  
__inout_bcount_full (*dimensioni*)  
__inout_bcount_full_opt (*dimensioni*)  
__inout_bcount_opt (*dimensioni*)  
__inout_bcount_part (*dimensioni*,*lunghezza*)  
__inout_bcount_part_opt (*dimensioni*,*lunghezza*)  
__inout_ecount (*dimensioni*)  
__inout_ecount_full (*dimensioni*)  
__inout_ecount_full_opt (*dimensioni*)  
__inout_ecount_opt (*dimensioni*)  
__inout_ecount_part (*dimensioni*,*lunghezza*)  
__inout_ecount_part_opt (*dimensioni*,*lunghezza*)  
__inout_opt  
__out  
__out_bcount (*dimensioni*)  
__out_bcount_full (*dimensioni*)  
__out_bcount_full_opt (*dimensioni*)  
__out_bcount_opt (*dimensioni*)  
__out_bcount_part (*dimensioni*,*lunghezza*)  
__out_bcount_part_opt (*dimensioni*,*lunghezza*)  
__out_ecount (*dimensioni*)  
__out_ecount_full (*dimensioni*)  
__out_ecount_full_opt (*dimensioni*)  
__out_ecount_opt (*dimensioni*)  
__out_ecount_part (*dimensioni*,*lunghezza*)  
__out_ecount_part_opt (*dimensioni*,*lunghezza*)  
__out_opt  

## <a name="advanced-annotations"></a>Annotazioni avanzate

Le annotazioni avanzate forniscono informazioni aggiuntive sul parametro o sul valore restituito. Ogni parametro o valore restituito può utilizzare una o più annotazioni avanzate.



| Annotazione                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn (*risorsa*)<br/> | Le funzioni vengono bloccate sulla risorsa specificata.<br/>                                                                                                                                                                                                                      |
| <span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback<br/>                                                                        | La funzione può essere usata come puntatore a funzione.<br/>                                                                                                                                                                                                                      |
| <span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn<br/>                               | I chiamanti devono controllare il valore restituito.<br/>                                                                                                                                                                                                                                 |
| <span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_stringa di formato \_<br/>                                                        | Il parametro è una stringa che contiene i marcatori% di tipo printf.<br/>                                                                                                                                                                                                      |
| <span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in \_ awcount (*expr*,*size*)<br/>                            | Se l'espressione è true all'uscita, la dimensione del buffer di input viene specificata in byte. Se l'espressione è false, la dimensione viene specificata in Elements.<br/>                                                                                                                |
| <span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated<br/>                                          | È possibile accedere al buffer fino a includere la prima sequenza di due caratteri **null** o puntatori.<br/>                                                                                                                                                            |
| <span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated<br/>                                                      | È possibile accedere al buffer fino a includere il primo carattere o puntatore **null** .<br/>                                                                                                                                                                              |
| <span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*size*)<br/>                         | Se l'espressione è true all'uscita, la dimensione del buffer di output viene specificata in byte. Se l'espressione è false, la dimensione viene specificata in Elements. <br/>                                                                                                              |
| <span id="__override"></span><span id="__OVERRIDE"></span>\_\_override<br/>                                                                        | Specifica il comportamento di override di tipo C# per i metodi virtuali.<br/>                                                                                                                                                                                                           |
| <span id="__reserved"></span><span id="__RESERVED"></span>\_\_riservati<br/>                                                                        | Il parametro è riservato per utilizzi futuri e deve essere zero o **null**.<br/>                                                                                                                                                                                               |
| <span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_operazione riuscita (*expr*)<br/>                                                       | Se l'espressione è true all'uscita, il chiamante può basarsi su tutte le garanzie specificate da altre annotazioni. Se l'espressione è false, il chiamante non può basarsi sulle garanzie. Questa annotazione viene aggiunta automaticamente alle funzioni che restituiscono un valore **HRESULT** .<br/> |
| <span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)<br/>                                                    | Considera il parametro come il tipo specificato anziché il tipo dichiarato.<br/>                                                                                                                                                                                             |



 

Negli esempi seguenti vengono illustrati il buffer e le annotazioni avanzate per le funzioni [**DeleteTimerQueueTimer ha provocato**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)e [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .


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

 

