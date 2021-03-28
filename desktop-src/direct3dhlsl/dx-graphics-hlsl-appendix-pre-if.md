---
title: " Direttive if, elif, else e endif"
description: Direttive per il preprocessore che controllano la compilazione di parti di un file di origine.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Direttive if, elif, else e endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32206232c726f19febf77c3f3270882894a6747
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117770"
---
# <a name="if-elif-else-and-endif-directives"></a>\#\#direttive if, elif, \# else e \# endif

Direttive per il preprocessore che controllano la compilazione di parti di un file di origine.



| \#Se *ifCondition* ...         |
|--------------------------------|
| \[\#Elif *elifCondition* ...\] |
| \[\#altrimenti...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condizione primaria da valutare. Se questo parametro restituisce un valore diverso da zero, l'intero testo tra la \# direttiva if e l'istanza successiva della \# direttiva elif, \# else o \# endif viene mantenuto nell'unità di conversione. in caso contrario, il codice sorgente successivo non viene mantenuto. <br/> La condizione può utilizzare l'operatore del preprocessore definito per determinare se una specifica costante o macro del preprocessore è definita. Questo utilizzo è equivalente all'utilizzo della direttiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Vedere la sezione Osservazioni per le restrizioni relative al valore del parametro *ifCondition* . <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ opzionale\] <br/> | Altra condizione da valutare. Se il parametro *ifCondition* e tutte le \# direttive elif precedenti restituiscono zero e questo parametro restituisce un valore diverso da zero, tutto il testo tra la \# direttiva elif e l'istanza successiva della \# direttiva elif, \# else o \# endif verrà mantenuto nell'unità di conversione. in caso contrario, il codice sorgente successivo non verrà mantenuto. <br/> La condizione può utilizzare l'operatore del preprocessore definito per determinare se una specifica costante o macro del preprocessore è definita. Questo utilizzo è equivalente all'utilizzo della direttiva [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md) . <br/> Vedere la sezione Osservazioni per le restrizioni relative al valore del parametro *elifCondition* . <br/> |



 

## <a name="remarks"></a>Commenti

Ogni \# direttiva if in un file di origine deve corrispondere a una \# direttiva endif di chiusura. È possibile visualizzare un numero qualsiasi di \# direttive elif tra le \# \# direttive if e endif, ma \# è consentita al massimo una direttiva else. La \# direttiva else, se presente, deve essere l'ultima direttiva prima di \# endif. Le direttive di compilazione condizionale contenute nei file di inclusione devono soddisfare le stesse condizioni.

Le \# \# direttive if, elif, \# else e \# endif possono annidarsi nelle parti di testo di altre \# direttive if. Ogni \# direttiva else, \# elif o endif annidata \# appartiene alla direttiva If precedente più vicina \# .

Se nessuna condizione restituisce un valore diverso da zero, il preprocessore seleziona il blocco di testo dopo la \# direttiva else. Se la \# clausola Else viene omessa e nessuna condizione restituisce un valore diverso da zero, non viene selezionato alcun blocco di testo.

I parametri *ifCondition* e *elifCondition* soddisfano i requisiti seguenti:

-   Le espressioni di compilazione condizionale vengono considerate come valori [**Long con segno**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) e queste espressioni vengono valutate utilizzando le stesse regole delle espressioni in C++.
-   Le espressioni devono disporre di un tipo integrale e possono includere solo costanti Integer, costanti carattere e l'operatore defined.
-   Le espressioni non possono usare **sizeof** o un operatore di cast di tipo.
-   È possibile che l'ambiente di destinazione non sia in grado di rappresentare tutti gli intervalli di Integer.
-   La traduzione rappresenta il tipo [**int**](/windows/desktop/WinProg/windows-data-types) allo stesso modo del tipo **Long** e [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) equivale a **unsigned long**.
-   Il convertitore può traslare le costanti carattere in un set di valori di codice diverso dal set per l'ambiente di destinazione. Per determinare le proprietà dell'ambiente di destinazione, verificare i valori delle macro da LIMITS.H in un'applicazione sviluppata per l'ambiente di destinazione.
-   L'espressione non deve eseguire alcuna analisi di ambiente e deve rimanere isolata dai dettagli di implementazione nel computer di destinazione.

## <a name="examples"></a>Esempio

Questa sezione contiene esempi che illustrano come usare le direttive per il preprocessore di compilazione condizionale.

### <a name="use-of-the-defined-operator"></a>Utilizzo dell'operatore definito

Nell'esempio seguente viene illustrato l'utilizzo dell'operatore definito. Se viene definito il credito dell'identificatore, viene compilata la chiamata alla funzione di **credito** . Se viene definito il debito dell'identificatore, viene compilata la chiamata alla funzione di **debito** . Se non viene definito alcun identificatore, viene compilata la chiamata alla funzione **printerror** . Si noti che "CREDIT" e "Credit" sono identificatori distinti in C e C++ perché i casi sono diversi.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Uso delle \# direttive if annidate

Nell'esempio seguente viene illustrato come annidare le \# direttive if. In questo esempio si presuppone che sia stata definita in precedenza una costante simbolica denominata DLEVEL. Le \# \# direttive elif e else vengono usate per effettuare una delle quattro scelte, in base al valore di DLEVEL. Lo STACK di costanti è impostato su 0, 100 o 200, a seconda della definizione di DLEVEL. Se DLEVEL è maggiore di 5, STACK non è definito.


```
#if DLEVEL > 5
    #define SIGNAL  1
    #if STACKUSE == 1
        #define STACK   200
    #else
        #define STACK   100
    #endif
#else
    #define SIGNAL  0
    #if STACKUSE == 1
        #define STACK   100
    #else
        #define STACK   50
    #endif
#endif
#if DLEVEL == 0
    #define STACK 0
#elif DLEVEL == 1
    #define STACK 100
#elif DLEVEL > 5
    display( debugptr );
#else
    #define STACK 200
#endif
```



### <a name="use-for-including-header-files"></a>Usare per includere i file di intestazione

Generalmente la compilazione condizionale viene utilizzata per evitare più inclusioni dello stesso file di intestazione. In C++, in cui le classi sono spesso definite in file di intestazione, è possibile usare costrutti di compilazione condizionale per impedire più definizioni. Nell'esempio seguente viene determinato se è definita la costante simbolica di esempio \_ H. In tal caso, il file è già stato incluso e non deve essere rielaborato; in caso contrario, \_ viene definita la costante di esempio H per indicare l'esempio. H è già stato elaborato.


```
#if !defined( EXAMPLE_H )
#define EXAMPLE_H

class Example
{
...
};

#endif // !defined( EXAMPLE_H )
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

