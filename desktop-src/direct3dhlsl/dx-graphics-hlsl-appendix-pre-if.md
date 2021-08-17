---
title: " Direttive if, elif, else ed endif"
description: Direttive del preprocessore che controllano la compilazione di parti di un file di origine.
ms.assetid: f29e5a9b-cc0c-4fca-aac7-809a226eda58
keywords:
- Direttive if, elif, else ed endif HLSL
topic_type:
- apiref
api_name:
- if, elif, else, and endif Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb5f4716509905d4ce800abbe4cb11b85d116d7a5afd5a56301b1ecb5ce0724b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726451"
---
# <a name="if-elif-else-and-endif-directives"></a>\#Direttive if, \# \# elif, else ed \# endif

Direttive del preprocessore che controllano la compilazione di parti di un file di origine.



| \#if *ifCondition* ...         |
|--------------------------------|
| \[\#elif *elifCondition* ...\] |
| \[\#Altro...\]                 |
| \#endif                        |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ifCondition"></span><span id="ifcondition"></span><span id="IFCONDITION"></span>*ifCondition*<br/>                                                                                   | Condizione primaria da valutare. Se questo parametro restituisce un valore diverso da zero, tutto il testo compreso tra questa direttiva if e l'istanza successiva della direttiva elif, else o endif viene mantenuto nell'unità di conversione; in caso contrario, il codice sorgente successivo non viene \# \# \# \# mantenuto. <br/> La condizione può usare l'operatore del preprocessore definito per determinare se è definita una macro o una costante del preprocessore specifica. questo utilizzo equivale all'uso della [ \# direttiva ifdef.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Vedere la sezione Osservazioni per le restrizioni sul valore del *parametro ifCondition.* <br/>                                                                                        |
| <span id="elifCondition__optional__________"></span><span id="elifcondition__optional__________"></span><span id="ELIFCONDITION__OPTIONAL__________"></span>*elifCondition* \[ Opzionale\] <br/> | Altra condizione da valutare. Se il parametro *ifCondition* e tutte le direttive elif precedenti restituiscono zero e questo parametro restituisce un valore diverso da zero, tutto il testo tra questa direttiva elif e l'istanza successiva della direttiva \# elif, else o endif viene mantenuto nell'unità di conversione. In caso contrario, il codice sorgente successivo non viene \# \# \# \# mantenuto. <br/> La condizione può usare l'operatore del preprocessore definito per determinare se è definita una macro o una costante del preprocessore specifica. questo utilizzo equivale all'uso della [ \# direttiva ifdef.](dx-graphics-hlsl-appendix-pre-ifdef.md) <br/> Vedere la sezione Osservazioni per le restrizioni sul valore del *parametro elifCondition.* <br/> |



 

## <a name="remarks"></a>Commenti

Ogni \# direttiva if in un file di origine deve corrispondere a una direttiva \# endif di chiusura. Tra le direttive if ed endif può essere presente un numero qualsiasi di direttive elif, ma è consentita al massimo \# \# una direttiva \# \# else. La \# direttiva else, se presente, deve essere l'ultima direttiva prima \# di endif. Le direttive di compilazione condizionale contenute nei file di inclusione devono soddisfare le stesse condizioni.

Le \# direttive \# if, elif, else ed endif possono annidare nelle parti di testo di \# altre direttive \# \# if. Ogni \# direttiva else, elif o endif annidata \# appartiene alla direttiva if precedente più \# \# vicina.

Se nessuna condizione restituisce un valore diverso da zero, il preprocessore seleziona il blocco di testo dopo la \# direttiva else. Se la clausola else viene omessa e nessuna condizione restituisce un valore \# diverso da zero, non viene selezionato alcun blocco di testo.

I *parametri ifCondition* *ed elifCondition* soddisfano in modo molto i requisiti seguenti:

-   Le espressioni di compilazione condizionale vengono [**considerate come**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) valori long con segno e vengono valutate usando le stesse regole delle espressioni in C++.
-   Le espressioni devono disporre di un tipo integrale e possono includere solo costanti Integer, costanti carattere e l'operatore defined.
-   Le espressioni non possono **usare sizeof** o un operatore di cast di tipo.
-   È possibile che l'ambiente di destinazione non sia in grado di rappresentare tutti gli intervalli di Integer.
-   La conversione rappresenta [**il tipo int**](/windows/desktop/WinProg/windows-data-types) come il tipo **long** e [**unsigned int**](https://msdn.microsoft.com/library/cc953fe1(v=VS.71).aspx) come **unsigned long.**
-   Il convertitore può traslare le costanti carattere in un set di valori di codice diverso dal set per l'ambiente di destinazione. Per determinare le proprietà dell'ambiente di destinazione, verificare i valori delle macro da LIMITS.H in un'applicazione sviluppata per l'ambiente di destinazione.
-   L'espressione non deve eseguire alcuna analisi di ambiente e deve rimanere isolata dai dettagli di implementazione nel computer di destinazione.

## <a name="examples"></a>Esempio

Questa sezione contiene esempi che illustrano come usare le direttive del preprocessore di compilazione condizionale.

### <a name="use-of-the-defined-operator"></a>Uso dell'operatore definito

Nell'esempio seguente viene illustrato l'utilizzo dell'operatore definito. Se l'identificatore CREDIT è definito, la chiamata alla funzione **di credito** viene compilata. Se l'identificatore DEBIT è definito, la chiamata alla funzione **debit** viene compilata. Se nessuno dei due identificatori è definito, la chiamata alla **funzione printerror** viene compilata. Si noti che "CREDIT" e "credit" sono identificatori distinti in C e C++ perché i relativi case sono diversi.


```
#if defined(CREDIT)
    credit();
#elif defined(DEBIT)
    debit();
#else
    printerror();
#endif
```



### <a name="use-of-nested-if-directives"></a>Uso di direttive \# if annidate

Nell'esempio seguente viene illustrato come annidare \# le direttive if. In questo esempio si presuppone che sia stata definita in precedenza una costante simbolica denominata DLEVEL. Le direttive elif ed else vengono usate per effettuare una delle quattro scelte seguenti, in \# base al valore di \# DLEVEL. La costante STACK è impostata su 0, 100 o 200, a seconda della definizione di DLEVEL. Se DLEVEL è maggiore di 5, STACK non è definito.


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

Generalmente la compilazione condizionale viene utilizzata per evitare più inclusioni dello stesso file di intestazione. In C++, in cui le classi vengono spesso definite nei file di intestazione, è possibile usare costrutti di compilazione condizionale per impedire più definizioni. Nell'esempio seguente viene determinato se è definita la costante simbolica EXAMPLE \_ H. In tal caso, il file è già stato incluso e non deve essere rielaborato. In caso contrario, la costante EXAMPLE \_ H viene definita per indicare tale EXAMPLE. H è già stato elaborato.


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

 

