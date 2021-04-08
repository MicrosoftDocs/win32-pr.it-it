---
title: Differenze tra MIDL e MkTypLib
description: Differenze tra MIDL e MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL e FAD MIDL, differenze tra MIDL e MkTypLib
- MIDL MkTypLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045355"
---
# <a name="differences-between-midl-and-mktyplib"></a>Differenze tra MIDL e MkTypLib

> [!Note]  
> Lo strumento Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL.

 

Esistono alcune aree principali in cui il compilatore MIDL è diverso da MkTypLib. La maggior parte di queste differenze si verifica perché MIDL è orientato più verso la sintassi C rispetto a MkTypLib.

In generale, è consigliabile usare la sintassi MIDL nei file IDL. Tuttavia, se è necessario compilare un file FAD esistente o in caso contrario mantenere la compatibilità con MkTypLib, usare l'opzione del compilatore MIDL [**/mktyplib203**](-mktyplib203.md) per forzare il comportamento di midl come Mkktyplib.exe, versione 2,03. (Si tratta dell'ultima versione dello strumento MkTypLib). In particolare, l'opzione **/mktyplib203** risolve le differenze seguenti:

-   sintassi typedef per i tipi di dati complessi

    In MkTypLib entrambe le definizioni seguenti generano un record TKIND \_ per "questo \_ struct" nella libreria dei tipi. Il tag "struct \_ tag" è facoltativo e, se usato, non verrà visualizzato nella libreria dei tipi.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Se manca un tag facoltativo, MIDL lo genererà aggiungendo un tag alla definizione fornita dall'utente. Poiché la prima definizione include un tag, MIDL genererà un \_ record TKIND per "questo \_ struct" e un \_ alias TKIND per "questo struct \_ " (definendo " \_ struct" come alias per "struct \_ tag"). Poiché il tag non è presente nella seconda definizione, MIDL genererà un \_ record TKIND per un nome modificato, interno a MIDL, che non è significativo per l'utente e un alias TKIND \_ per "tale \_ struct".

    Ciò ha implicazioni potenziali per i browser della libreria dei tipi che visualizzano semplicemente il nome di un record nell'interfaccia utente. Se si prevede che un \_ record TKIND abbia un nome reale, nell'interfaccia utente potrebbero essere presenti nomi non riconoscibili. Questo comportamento si applica anche alle definizioni di [**Union**](union.md) e [**enum**](enum.md) , con il compilatore MIDL che genera \_ rispettivamente le unioni TKIND e le \_ enumerazioni TKIND.

    MIDL consente inoltre le definizioni di [**struct**](struct.md), [**Union**](union.md)e [**enum**](enum.md) di tipo C. La definizione seguente, ad esempio, è valida in MIDL:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   tipi di dati Boolean

    In MkTypLib, il tipo di base [**booleano**](boolean.md) e il tipo di dati MkTypLib bool corrispondono a VT \_ bool, che esegue il mapping a Variant \_ bool e che è definito come [**short**](short.md). In MIDL il tipo di base **booleano** è equivalente a VT \_ Ui1, che è definito come [**unsigned char**](unsigned.md)e il tipo di dati bool è definito come [**Long**](long.md). Ciò comporta difficoltà se si combinano la sintassi di IDL e la sintassi di gestione delle funzioni di gestione delle funzioni nello stesso file, cercando comunque di mantenere la compatibilità con MkTypLib. Poiché i tipi di dati hanno dimensioni diverse, il codice di marshalling non corrisponderà a quanto descritto nelle informazioni sul tipo. Se si desidera un valore \_ bool di VT nella libreria dei tipi, è necessario utilizzare il \_ tipo di dati bool Variant.

-   Definizioni GUID nei file di intestazione

    In MkTypLib i GUID vengono definiti nel file di intestazione con una macro che può essere compilata in modo condizionale per generare una predefinizione GUID o un GUID di cui è stata creata un'istanza. MIDL in genere inserisce le predefinizioni GUID nei file di intestazione e nelle creazioni GUID generate solo nel file generato dall'opzione [**/IID**](-iid.md) .

Le differenze di comportamento seguenti non possono essere risolte tramite l'opzione [**/mktyplib203**](-mktyplib203.md) :

-   Maiuscole/minuscole

    MIDL fa distinzione tra maiuscole e minuscole. l'automazione OLE non lo è.

-   Ambito dei simboli in una dichiarazione di enumerazione

    In MkTypLib l'ambito dei simboli in un'enumerazione è local. In MIDL l'ambito dei simboli in un'enumerazione è globale, così com'è in C. Il codice seguente, ad esempio, verrà compilato in MkTypLib, ma genererà un errore di nome duplicato in MIDL:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Ambito dell'attributo pubblico

    Se si applica l'attributo [**public**](public.md) a un blocco di interfaccia, MkTypLib considera ogni typedef all'interno del blocco di interfaccia come Public. MIDL richiede che l'attributo **public** venga applicato in modo esplicito ai typedef che si desidera public.

-   Ordine di ricerca importlib

    Se si importano più librerie dei tipi e se queste librerie contengono riferimenti duplicati, MkTypLib risolve questo problema utilizzando il primo riferimento rilevato. MIDL utilizzerà l'ultimo riferimento rilevato. Se, ad esempio, si utilizza la seguente sintassi per la funzione di ricerca per indicizzazione, la libreria C utilizzerà il typedef MOO dalla libreria A se si compila con MkTypLib e il typedef di MOO dalla libreria B se si compila con MIDL:

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    La soluzione alternativa appropriata per questa operazione consiste nel qualificare ogni riferimento con il nome corretto della libreria di importazione, come segue:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   Tipo di dati VOID non riconosciuto

    MIDL riconosce il tipo di dati [**void**](void.md) del linguaggio C e non riconosce il tipo di dati void di automazione OLE. Se si dispone di un file FAD che usa VOID, inserire questa definizione all'inizio del file:

    ``` syntax
#define VOID void
    ```

-   Notazione esponenziale

    MIDL richiede che i valori espressi in notazione esponenziale siano contenuti tra virgolette. Ad esempio, "-2.5 E + 3"

-   Valori LCID e costanti

    In genere MIDL non considera l'LCID durante l'analisi dei file. Per forzare questo comportamento per un valore o se è necessario usare la notazione specifica delle impostazioni locali durante la definizione di una costante, racchiudere il valore o la costante tra virgolette.

Per ulteriori informazioni, vedere [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)e [marshalling dei tipi di dati OLE](marshaling-ole-data-types.md).

 

 




