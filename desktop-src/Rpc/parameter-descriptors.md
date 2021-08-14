---
title: Descrittori di parametri
description: Come accennato in precedenza, \ 8211;Oi e \ 8211;I descrittori dei parametri di stile Oif esistono.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a13b052d49629333bd9cb121b4d1b661722cb3a7a69ad2a17d3e2740a0cd8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927550"
---
# <a name="parameter-descriptors"></a>Descrittori di parametri

Come accennato in [**precedenza,**](/windows/desktop/Midl/-oi) esistono descrittori di parametro di stile **–Oi e –Oif.**

## <a name="the-oi-parameter-descriptors"></a>Descrittori dei parametri –Oi

Gli stub completamente interpretati richiedono informazioni aggiuntive per ognuno dei parametri in una chiamata RPC. Le descrizioni dei parametri di una routine seguono immediatamente dopo la descrizione della procedura.

[**Semplice -Oi**](/windows/desktop/Midl/-oi)

**Descrittori di parametri**

Il formato per la descrizione di un parametro di tipo semplice \[ **in** \] o restituito è:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

–oppure–

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Dove tipo \_ semplice<1> è il token FC che indica il tipo semplice. I codici sono i seguenti:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Altro -Oi**

**Descrittori di parametri**

Il formato della descrizione per tutti gli altri tipi di parametro è:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Dove la direzione del parametro<1> campo per ognuna di queste descrizioni deve essere una di quelle illustrate \_ nella tabella seguente.



| Hex | Contrassegno                          | Significato                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ IN \_ PARAM                 | Parametro in.                                            |
| 50  | FC \_ IN \_ OUT \_ PARAM            | Parametro in/out.                                        |
| 51  | FC \_ OUT \_ PARAM                | Parametro out.                                           |
| 52  | FC \_ RETURN \_ PARAM             | Valore restituito dalla routine.                                   |
| 4f  | FC \_ IN \_ PARAM \_ NO \_ FREE \_ INST | Oggetto in xmit/rep come parametro per il quale non viene effettuata alcuna liberatura. |



 

La dimensione dello stack<1> è la dimensione del parametro nello stack, espressa come numero di numeri interi che il parametro occupa \_ nello stack.

> [!Note]  
> La [**modalità –Oi**](/windows/desktop/Midl/-oi) non è supportata nelle piattaforme a 64 bit.

 

L'offset<2> campo è l'offset nella tabella della stringa di formato del tipo, che indica il descrittore di tipo \_ per l'argomento.

## <a name="the-oif-parameter-descriptors"></a>Descrittori di parametri –Oif

Esistono due formati possibili per la descrizione di un parametro, uno per i tipi di base, un altro per tutti gli altri tipi.

Tipi di base:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

Altro:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

In entrambi gli offset dello stack<2> indica l'offset nello stack di \_ argomenti virtuali, in byte. Per i tipi di base, il tipo di argomento viene fornito direttamente dal carattere di formato corrispondente al tipo. Per altri tipi, l'offset del tipo<2> campo fornisce l'offset nella tabella della stringa di formato del tipo in cui si trova il descrittore di tipo per \_ l'argomento.

Il campo dell'attributo del parametro è definito come segue:

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   Il bit **MustSize** viene impostato solo se il parametro deve essere ridimensionato.
-   Il bit **MustFree** viene impostato se il server deve chiamare la routine NdrFree del \* parametro.
-   Il bit **IsSimpleRef** è impostato per un parametro che è un puntatore di riferimento a un puntatore diverso da un altro puntatore e che non dispone di attributi di allocazione. Per un tipo di questo tipo, l'offset del tipo della descrizione del parametro<> campo, ad eccezione di un puntatore di riferimento a un tipo di base, fornisce l'offset per il tipo del riferimento. Il puntatore di riferimento viene semplicemente \_ ignorato.
-   Il bit **IsDontCallFreeInst** è impostato per determinati parametri che rappresentano come parametri le cui routine di istanza libera \_ non devono essere chiamate.
-   I bit **ServerAllocSize** sono diversi da zero se il parametro è \[  \] \[ out, **in** o in, puntatore a puntatore a enum16 o puntatore a enum16 e verrà inizializzato nello \] \[  \] stack dell'interprete del server, **\_** anziché usare una chiamata a I RpcAllocate . Se diverso da zero, questo valore viene moltiplicato per 8 per ottenere il numero di byte per il parametro . Si noti che in questo modo per un puntatore vengono sempre allocati almeno 8 byte.
-   Il bit **IsBasetype** è impostato per i tipi semplici di cui viene effettuato il marshalling dal ciclo dell'interprete [**main -Oif.**](/windows/desktop/Midl/-oi) In particolare, un tipo semplice con un attributo di intervallo non viene contrassegnato come tipo di base per forzare il marshalling della routine di intervallo tramite l'invio tramite un token FC \_ RANGE.
-   Il bit **IsByValue** è impostato per i tipi composti inviati per valore, ma non per i tipi semplici, indipendentemente dal fatto che l'argomento sia un puntatore. I tipi composti per cui è impostata sono strutture, unioni, [**trasmissione \_**](/windows/desktop/Midl/transmit-as)come , [**rappresentano \_ come**](/windows/desktop/Midl/represent-as), [**wire \_ marshal**](/windows/desktop/Midl/wire-marshal) e SAFEARRAY. In generale, il bit è stato introdotto a vantaggio del ciclo dell'interprete principale nell'interprete [**–Oicf,**](/windows/desktop/Midl/-oi) per garantire la corretta dereferenziazione degli argomenti non di tipo composto. Questo bit non è mai stato usato nelle versioni precedenti dell'interprete.

 

 