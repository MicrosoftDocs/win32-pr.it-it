---
title: Differenze tra MIDL e MkTypLib
description: Differenze tra MIDL e MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL e ODL MIDL , differenze tra MIDL e MkTypLib
- MkTypLib MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ae20e00dab492a140f48c9de683abeac04676824bd6513ccf086889b4460e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643625"
---
# <a name="differences-between-midl-and-mktyplib"></a>Differenze tra MIDL e MkTypLib

> [!Note]  
> Lo Mktyplib.exe è obsoleto. In alternativa, usare il compilatore MIDL.

 

Esistono alcune aree chiave in cui il compilatore MIDL differisce da MkTypLib. La maggior parte di queste differenze si verifica perché MIDL è orientato più verso la sintassi C rispetto a MkTypLib.

In generale, è necessario usare la sintassi MIDL nei file IDL. Se tuttavia è necessario compilare un file ODL esistente o mantenere la compatibilità con MkTypLib, usare l'opzione del compilatore [**MIDL /mktyplib203**](-mktyplib203.md) per forzare il comportamento di MIDL come Mkktyplib.exe versione 2.03. Si tratta dell'ultima versione dello strumento MkTypLib. In particolare, **l'opzione /mktyplib203** risolve queste differenze:

-   Sintassi typedef per tipi di dati complessi

    In MkTypLib entrambe le definizioni seguenti generano un record TKIND \_ per "this \_ struct" nella libreria dei tipi. Il tag "tag struct" è facoltativo e, se usato, non \_ verrà visualizzato nella libreria dei tipi.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Se manca un tag facoltativo, MIDL lo genera, aggiungendo di fatto un tag alla definizione fornita dall'utente. Poiché la prima definizione ha un tag , MIDL genererà un record TKIND per "this struct" e un ALIAS TKIND per \_ \_ \_ "this \_ struct" (definendo "this struct" come alias per \_ "struct \_ tag"). Poiché il tag non è presente nella seconda definizione, MIDL genererà un record TKIND per un nome non valido, interno a MIDL, che non è significativo per l'utente e un ALIAS TKIND per \_ \_ \_ "tale struct".

    Ciò può avere implicazioni potenziali per i browser delle librerie dei tipi che mostrano semplicemente il nome di un record nell'interfaccia utente. Se si prevede che un record TKIND abbia un nome reale, è possibile che nell'interfaccia utente vengano visualizzati nomi \_ non riconoscibili. Questo comportamento si applica [](enum.md) anche alle [**definizioni**](union.md) di unione ed enumerazione, con il compilatore MIDL che genera rispettivamente UNION TKIND e \_ TKIND \_ ENUM.

    MIDL consente anche definizioni di [**struct**](struct.md), [**union**](union.md) [**ed enum di tipo**](enum.md) C. Ad esempio, la definizione seguente è valida in MIDL:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   tipi di dati Boolean

    In MkTypLib, il tipo [**di**](boolean.md) base booleano e il tipo di dati MkTypLib BOOL equi equipano a VT BOOL, che esegue il mapping \_ a VARIANT BOOL e che è definito come \_ [**short**](short.md). In MIDL il tipo **di** base booleano è equivalente a VT UI1, definito come char senza segno, e il tipo di dati BOOL è definito \_ come [**long.**](long.md) [](unsigned.md) Ciò comporta difficoltà se si combinano la sintassi IDL e la sintassi ODL nello stesso file, pur tentando di mantenere la compatibilità con MkTypLib. Poiché i tipi di dati sono di dimensioni diverse, il codice di marshalling non corrisponderà a quanto descritto nelle informazioni sul tipo. Se si vuole un boOL VT nella libreria dei tipi, è necessario usare il tipo di dati \_ VARIANT \_ BOOL.

-   Definizioni GUID nei file di intestazione

    In MkTypLib, i GUID sono definiti nel file di intestazione con una macro che può essere compilata in modo condizionale per generare un GUID predefinito o un GUID di cui è stata creata un'istanza. MIDL in genere inserisce le predefiniti GUID nei file di intestazione generati e nelle istanze guid solo nel file generato [**dall'opzione /iid.**](-iid.md)

Le differenze di comportamento seguenti non possono essere risolte tramite [**l'opzione /mktyplib203:**](-mktyplib203.md)

-   Maiuscole/minuscole

    MIDL fa distinzione tra maiuscole e minuscole, l'automazione OLE no.

-   Ambito dei simboli in una dichiarazione di enumerazione

    In MkTypLib l'ambito dei simboli in un'enumerazione è locale. In MIDL l'ambito dei simboli in un'enumerazione è globale, come in C. Ad esempio, il codice seguente verrà compilato in MkTypLib, ma genererà un errore di nome duplicato in MIDL:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Ambito dell'attributo public

    Se si applica [**l'attributo public**](public.md) a un blocco di interfaccia, MkTypLib considera tutti i typedef all'interno di tale blocco di interfaccia come pubblici. MIDL richiede l'applicazione esplicita **dell'attributo public** ai typedef che si vuole pubblicare.

-   Ordine di ricerca di Importlib

    Se si importano più librerie dei tipi e queste librerie contengono riferimenti duplicati, MkTypLib risolve il problema usando il primo riferimento trovato. MIDL userà l'ultimo riferimento trovato. Ad esempio, data la sintassi ODL seguente, la libreria C userà il typedef MOO della libreria A se si esegue la compilazione con MkTypLib e il typedef MOO dalla libreria B se si esegue la compilazione con MIDL:

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

    La soluzione alternativa appropriata consiste nel qualificare ogni riferimento con il nome della libreria di importazione corretto, come nel seguente:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   Tipo di dati VOID non riconosciuto

    MIDL riconosce il tipo di dati [**void nel linguaggio**](void.md) C e non riconosce il tipo di dati VOID di automazione OLE. Se si dispone di un file ODL che usa VOID, inserire questa definizione all'inizio del file:

    ``` syntax
#define VOID void
    ```

-   Notazione esponenziale

    MIDL richiede che i valori espressi in notazione esponenziale siano contenuti tra virgolette. Ad esempio, "-2.5E+3"

-   Valori e costanti LCID

    In genere MIDL non considera l'LCID durante l'analisi dei file. Per forzare questo comportamento per un valore o se è necessario usare la notazione specifica delle impostazioni locali quando si definisce una costante, racchiudere il valore o la costante tra virgolette.

Per altre informazioni, vedere [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md)e [Marshalling dei tipi di dati OLE.](marshaling-ole-data-types.md)

 

 




