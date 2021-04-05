---
title: Descrittori di parametro
description: Come indicato in precedenza, 8211; OI e \ 8211; descrittori di parametro di stile OIF sono disponibili.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729410"
---
# <a name="parameter-descriptors"></a>Descrittori di parametro

Come indicato in precedenza, esistono descrittori di parametro di stile [**– OI**](/windows/desktop/Midl/-oi) e **– OIF** .

## <a name="the-oi-parameter-descriptors"></a>Descrittori di parametro – OI

Gli stub completamente interpretati richiedono informazioni aggiuntive per ogni parametro in una chiamata RPC. Le descrizioni dei parametri di una procedura seguono immediatamente dopo la descrizione della procedura.

[**Semplice-OI**](/windows/desktop/Midl/-oi)

**Descrittori di parametro**

Il formato per la descrizione di un \[  \] parametro di tipo semplice in o restituito è:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

–oppure–

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Dove il \_ tipo semplice<1> è il token FC che indica il tipo semplice. I codici sono i seguenti:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Altro-OI**

**Descrittori di parametro**

Il formato per la descrizione di tutti gli altri tipi di parametro è:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Dove la \_ direzione param<1> campo per ognuna di queste descrizioni deve essere uno dei seguenti elementi indicati nella tabella seguente.



| Hex | Contrassegno                          | Significato                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4D  | FC \_ in \_ param                 | Parametro in.                                            |
| 50  | FC \_ in \_ uscita \_ param            | Parametro in/out.                                        |
| 51  | \_param out \_ FC                | Parametro out.                                           |
| 52  | \_param return \_ FC             | Valore restituito di una routine.                                   |
| 4F  | FC \_ in \_ param \_ senza \_ \_ inst libero | Oggetto in Xmit/Rep come parametro per il quale non viene liberato. |



 

La dimensione dello stack \_<1> corrisponde alla dimensione del parametro nello stack, espressa come numero di numeri interi che il parametro occupa nello stack.

> [!Note]  
> La modalità [**-OI**](/windows/desktop/Midl/-oi) non è supportata nelle piattaforme a 64 bit.

 

L'offset del tipo \_<2> campo è l'offset nella tabella della stringa di formato del tipo, che indica il descrittore di tipo per l'argomento.

## <a name="the-oif-parameter-descriptors"></a>Descrittori di parametro – OIF

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

In entrambi \_ gli offset dello stack<2> indica l'offset nello stack di argomenti virtuale, espresso in byte. Per i tipi di base, il tipo di argomento viene fornito direttamente dal carattere di formato corrispondente al tipo. Per gli altri tipi, il \_ campo Offset tipo<2> fornisce l'offset nella tabella della stringa di formato del tipo in cui si trova il descrittore di tipo per l'argomento.

Il campo attributo parametro è definito come segue:

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
-   Se il server deve chiamare la routine NdrFree del parametro, viene impostato il bit **MustFree** \* .
-   Il bit **IsSimpleRef** è impostato per un parametro che è un puntatore di riferimento a un elemento diverso da un altro puntatore e senza attributi di allocazione. Per tale tipo, l'offset del tipo della descrizione del parametro \_<> campo, ad eccezione di un puntatore di riferimento a un tipo di base, fornisce l'offset al tipo di referente. il puntatore di riferimento viene semplicemente ignorato.
-   Il bit **IsDontCallFreeInst** è impostato per determinate rappresentazioni \_ come parametri le cui routine di istanza gratuite non devono essere chiamate.
-   I bit **ServerAllocSize** sono diversi da zero se il parametro è \[ **out** \] , \[ **in** \] o \[ **in, out** \] pointer to Pointer o pointer to enum16 e verrà inizializzato nello stack dell'interprete server, invece di usare una chiamata a **i \_ RpcAllocate**. Se è diverso da zero, questo valore viene moltiplicato per 8 per ottenere il numero di byte per il parametro. Si noti che questa operazione significa che almeno 8 byte vengono sempre allocati per un puntatore.
-   Il bit **IsBasetype** è impostato per i tipi semplici di cui viene eseguito il marshalling dal ciclo principale dell'interprete [**OIF**](/windows/desktop/Midl/-oi) . In particolare, un tipo semplice con un attributo di intervallo su di esso non è contrassegnato come tipo di base per forzare il marshalling della routine di intervallo tramite l'invio tramite un \_ token di intervallo FC.
-   Il bit **IsByValue** è impostato per i tipi composti inviati per valore, ma non è impostato per i tipi semplici, indipendentemente dal fatto che l'argomento sia un puntatore. I tipi composti per i quali è impostata sono strutture, unioni, [**trasmissione \_ come**](/windows/desktop/Midl/transmit-as), [**rappresentano \_ come**](/windows/desktop/Midl/represent-as), [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) e SAFEARRAY. In generale, il bit è stato introdotto per il vantaggio del ciclo dell'interprete principale nell'interprete [**-Oicf**](/windows/desktop/Midl/-oi) , per garantire che gli argomenti non semplici (definiti argomenti di tipo composto) siano dereferenziati correttamente. Questo bit non è mai stato usato nelle versioni precedenti dell'interprete.

 

 