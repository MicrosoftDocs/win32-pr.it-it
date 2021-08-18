---
title: Parola chiave union (RPC)
description: Le unioni richiedono parole chiave MIDL speciali per supportare l'uso con RPC (Remote Procedure Call).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fde18cca09f4db81af8eada2ae102a1bea373ed7859b3a7fc2bb9637f28d584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011009"
---
# <a name="union-keyword-rpc"></a>Parola chiave union (RPC)

Alcune funzionalità del linguaggio C, ad esempio le unioni, richiedono parole chiave MIDL speciali per supportare l'uso nelle chiamate di procedura remota. Un'unione nel linguaggio C è una variabile che contiene oggetti di tipi e dimensioni diversi. Lo sviluppatore crea in genere una variabile per tenere traccia dei tipi archiviati nell'unione. Per funzionare correttamente in un ambiente distribuito, anche la variabile che indica il tipo di unione o il *discriminante* deve essere disponibile per il computer remoto. MIDL fornisce il \[ [**tipo di \_ opzione**](/windows/desktop/Midl/switch-type) e switch è parole chiave per identificare il tipo e il \] nome non \[ [**\_**](/windows/desktop/Midl/switch-is) \] conformi.

MIDL richiede che il discriminante sia trasmesso con l'unione in uno dei due modi seguenti:

-   L'unione e la discriminante devono essere fornite come parametri.
-   L'unione e la discriminante devono essere in pacchetto in una struttura .

MIDL fornisce due tipi fondamentali di unioni discriminanti: unione non incapsulata e [**\_**](/windows/desktop/Midl/nonencapsulated-unions) [**unione \_ incapsulata.**](/windows/desktop/Midl/encapsulated-unions) Il discriminante di un'unione non incapsulata è un altro parametro se l'unione è un parametro. È un altro campo se l'unione è un campo di una struttura. La definizione di un'unione incapsulata viene trasformata in una definizione di struttura il cui primo campo è il discriminante e il cui secondo e l'ultimo campo sono l'unione. L'esempio seguente illustra come fornire l'unione e la discriminante come parametri:

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

L'unione nell'esempio precedente può contenere un singolo valore: **short**, **float** o **char**. La definizione del tipo per l'unione include l'attributo del tipo **switch \_** MIDL che specifica il tipo di discriminante. In questo \[ caso, \_ switch type(short) \] specifica che il discriminante è di tipo **short.** L'opzione deve essere di tipo Integer.

Se l'unione è un membro di una struttura , il discriminante deve essere un membro della stessa struttura. Se l'unione è un parametro, il discriminante deve essere un altro parametro. Il prototipo per **la funzione UnionParamProc** nell'esempio precedente mostra lo *sUtype* discriminante come ultimo parametro della chiamata. Il discriminante può essere visualizzato in qualsiasi posizione nella chiamata. Il tipo del parametro specificato **\[ nell'opzione è l'attributo \_ \]** deve corrispondere al tipo specificato **\[ nell'attributo del \_ tipo di \]** opzione.

L'esempio seguente illustra l'uso di una singola struttura che consente di creare un pacchetto del discriminante con l'unione:

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

Il compilatore MIDL RPC Microsoft consente dichiarazioni di unione all'esterno di [**costrutti typedef.**](/windows/desktop/Midl/typedef) Questa funzionalità è un'estensione di DCE IDL. Per altre informazioni, vedere [**union**](/windows/desktop/Midl/union).

 

 