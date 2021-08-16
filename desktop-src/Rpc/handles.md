---
title: Selettori
description: Nella descrizione della stringa di formato di un handle di indirizzo di procedura sono presenti due parti.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb31dcf075b7b07b65d2a976a37386e164d8cadc11903a33c22172c433a3a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929538"
---
# <a name="handles"></a>Selettori

Nella descrizione della stringa di formato di un handle di indirizzo di procedura sono presenti due parti. La prima parte è il tipo di handle<1> campo della descrizione di una routine, usato per \_ indicare handle impliciti. Questa parte è sempre presente. La seconda parte è una descrizione di parametro di qualsiasi handle esplicito nella procedura. Entrambe sono illustrate nelle sezioni seguenti, insieme a una descrizione del supporto aggiuntivo del compilatore MIDL della struttura del descrittore Stub per i problemi di handle di associazione.

## <a name="implicit-handles"></a>Handle impliciti

Se una routine usa un handle implicito per l'associazione, il tipo di handle<1> della descrizione della routine contiene uno dei tre valori \_ validi diversi da zero. Il supporto del compilatore MIDL per gli handle impliciti è disponibile nel campo IMPLICIT \_ HANDLE INFO della struttura \_ stub Descriptor:

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

Se la procedura usa un handle automatico, il **membro pAutoHandle** contiene l'indirizzo della variabile di handle auto definita dello stub.

Se la routine usa un handle primitivo implicito, il membro **pPrimitiveHandle** contiene l'indirizzo della variabile handle definita-primitiva dello stub.

Infine, se la routine usa un handle generico implicito, il **membro pGenericBindingInfo** contiene l'indirizzo del puntatore alla struttura **GENERIC BINDING \_ \_ INFO** corrispondente. La struttura di **dati MIDL \_ STUB \_ DESC contiene** un puntatore a una raccolta di strutture GENERIC BINDING **\_ \_ PAIR.** La voce nella posizione zero di questa raccolta è riservata per le routine **bind** e **unbind** corrispondenti all'handle di associazione generico a cui fa riferimento **pGenericBindingInfo** in **IMPLICIT HANDLE \_ \_ INFO**. Il tipo di handle di associazione implicito è indicato nella stringa di formato.

## <a name="explicit-handles"></a>Handle espliciti

Esistono tre tipi di handle espliciti: context, generic e primitive. Nel caso di un handle esplicito (o di un handle di contesto out only, gestito nello stesso modo), le informazioni sull'handle di associazione vengono visualizzate come uno dei \[  \] parametri della routine. Le tre possibili descrizioni sono le seguenti.

Primitiva

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

Il flag<1> indica se l'handle viene passato da un puntatore.

L'offset<2> l'offset dall'inizio dello stack all'handle primitivo.

> [!Note]  
> Una descrizione dell'handle primitivo nella stringa di formato del tipo viene ridotta a un singolo FC \_ IGNORE.

 

Generico

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

Il flag e le dimensioni<1> ha il flag superiore nibble e la dimensione \_ \_ inferiore nibble. Il flag indica se l'handle viene passato da un puntatore. Il campo size fornisce le dimensioni del tipo di handle generico definito dall'utente. Questa dimensione è limitata a 1, 2 o 4 byte nei sistemi a 32 bit e a 1, 2, 4 o 8 byte nei sistemi a 64 bit.

L'offset<2> campo fornisce l'offset dall'inizio dello stack del puntatore ai dati delle dimensioni specificate.

L'indice della coppia di routine di associazione<1> fornisce l'indice nel campo \_ \_ \_  aGenericBindingRoutinePairs del descrittore Stub ai puntatori di funzione di routine bind e **unbind** per l'handle generico.

> [!Note]  
> Una descrizione dell'handle generico nel formato del tipo è solo la descrizione del tipo di dati correlato.

 

Contesto

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

I flag<1> il modo in cui viene passato l'handle e il tipo. I flag validi sono indicati nella tabella seguente.



| Hex | Contrassegno                                   |
|-----|----------------------------------------|
| 80  | HANDLE \_ PARAM \_ È TRAMITE \_ \_ PTR            |
| 40  | HANDLE \_ PARAM \_ IS \_ IN                  |
| 20  | HANDLE \_ PARAM \_ IS \_ OUT                 |
| 21  | HANDLE \_ PARAM \_ IS \_ RETURN              |
| 08  | HANDLE DI CONTESTO \_ STRICT \_ NDR \_           |
| 04  | HANDLE DI \_ CONTESTO NDR \_ NO \_ \_ SERIALIZE    |
| 02  | SERIALIZZAZIONE \_ \_ DELL'HANDLE DEL CONTESTO \_ NDR        |
| 01  | \_L'HANDLE DEL CONTESTO \_ NDR NON PUÒ ESSERE \_ \_ \_ NULL |



 

I primi quattro flag sono sempre stati presenti, gli ultimi quattro sono stati aggiunti Windows 2000.

L'offset<2> campo fornisce l'offset dall'inizio dello stack all'handle di contesto.

L'indice della routine di rundown del contesto<1> fornisce un indice nel campo \_ \_ \_ **apfnNdrRundownRoutines** del descrittore Stub alla routine rundown usata per questo handle di contesto. Il compilatore genera sempre un indice. Per le routine che non hanno una routine rundown, si tratta di un indice in una posizione di tabella che contiene null.

Per gli stub incorporati in **–Oi2,** il parametro num<1> fornisce il conteggio ordinale, a partire da zero, specificando quale handle di contesto si trova \_ nella routine specificata.

Per le versioni precedenti dell'interprete, il parametro num<1> fornisce il numero di parametro dell'handle di contesto, a partire da \_ zero, nella relativa routine.

> [!Note]  
> Una descrizione dell'handle di contesto nella stringa di formato del tipo non avrà l'offset<2> nella descrizione.

 

## <a name="the-new-oif-header"></a>Nuova intestazione –Oif

Come accennato in precedenza, [**l'intestazione –Oif**](/windows/desktop/Midl/-oi) si espande nell'intestazione **–Oi.** Per praticità, tutti i campi sono visualizzati qui:

(intestazione precedente)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(estensioni [**–Oif)**](/windows/desktop/Midl/-oi)

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

La dimensione costante del buffer client<2> fornisce le dimensioni del buffer di marshalling che potrebbero essere state \_ \_ \_ pre-calcolate dal compilatore. Può trattarsi solo di una dimensione parziale, perché il flag ClientMustSize attiva il ridimensionamento.

La dimensione costante del buffer del server<2> fornisce le dimensioni del buffer di marshalling come \_ \_ \_ pre-ricalcolato dal compilatore. Può trattarsi solo di una dimensione parziale, perché il flag ServerMustSize attiva il ridimensionamento.

I FLAG OPT \_ INTERPRETER \_ sono definiti in Ndrtypes.h:

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   Il bit ServerMustSize viene impostato se il server deve eseguire un passaggio di dimensionamento del buffer.
-   Il bit ClientMustSize viene impostato se il client deve eseguire un passaggio di ridimensionamento del buffer.
-   Il bit HasReturn viene impostato se la routine ha un valore restituito.
-   Il bit HasPipes viene impostato se il pacchetto pipe deve essere usato per supportare un argomento pipe.
-   Il bit HasAsyncUuid viene impostato se la procedura è una procedura DCOM asincrona.
-   Il bit HasExtensions indica che vengono usate Windows 2000 e versioni successive.
-   Il bit HasAsyncHandle indica una procedura RPC asincrona.

Il bit HasAsyncHandle è stato inizialmente usato per un'implementazione DCOM diversa del supporto asincrono e pertanto non può essere usato per il supporto asincrono di stile corrente in DCOM. Il bit HasAsyncUuid attualmente lo indica.

 

 