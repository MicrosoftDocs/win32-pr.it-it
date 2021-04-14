---
title: Selettori
description: Fino a due parti nella descrizione della stringa di formato di un handle di indirizzo di una procedura.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338718"
---
# <a name="handles"></a>Selettori

Fino a due parti nella descrizione della stringa di formato di un handle di indirizzo di una procedura. La prima parte è il \_ tipo di handle<1> campo della descrizione di una stored procedure, usato per indicare gli handle impliciti. Questa parte è sempre presente. La seconda parte è una descrizione di parametro di qualsiasi handle esplicito nella procedura. Entrambe le sezioni riportate di seguito, insieme a una descrizione del supporto del compilatore MIDL aggiuntivo della struttura del descrittore stub per i problemi di gestione delle associazioni.

## <a name="implicit-handles"></a>Handle impliciti

Se una stored procedure utilizza un handle implicito per l'associazione, il tipo di handle \_<1> campo della descrizione della procedura contiene uno dei tre valori diversi da zero validi. Il supporto del compilatore MIDL per gli handle impliciti è disponibile nel \_ campo informazioni handle implicite \_ della struttura del descrittore Stub:

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

Se la stored procedure utilizza un handle automatico, il membro **pAutoHandle** contiene l'indirizzo della variabile dello stub definita-handle automatico.

Se la stored procedure utilizza un handle primitivo implicito, il membro **pPrimitiveHandle** contiene l'indirizzo della variabile di handle primitiva definita dallo stub.

Infine, se la stored procedure utilizza un handle generico implicito, il membro **pGenericBindingInfo** contiene l'indirizzo del puntatore alla struttura **di \_ \_ informazioni di associazione generica** corrispondente. La **\_ \_ Descrizione dello stub MIDL** della struttura di dati contiene un puntatore a una raccolta di strutture di **\_ \_ coppie di associazioni generiche** . La voce nella posizione zero di questa raccolta è riservata alle routine **Bind** e **UNBIND** corrispondenti all'handle di associazione generico a cui fa riferimento **PGenericBindingInfo** nelle **\_ \_ informazioni di handle implicite**. Il tipo di handle di associazione implicito è indicato nella stringa di formato.

## <a name="explicit-handles"></a>Handle espliciti

Esistono tre possibili tipi di handle espliciti: context, Generic e primitive. Nel caso di un handle esplicito (o un \[  \] handle del contesto solo in uscita, gestito allo stesso modo), le informazioni dell'handle di associazione vengono visualizzate come uno dei parametri della procedura. Le tre possibili descrizioni sono le seguenti.

Primitiva

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

Il flag<1> indica se l'handle viene passato da un puntatore.

L'offset<2> fornisce l'offset dall'inizio dello stack all'handle primitivo.

> [!Note]  
> Una descrizione dell'handle primitivo nella stringa di formato del tipo è ridotta a un singolo FC \_ Ignore.

 

Generico

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

Il flag \_ e le \_ dimensioni<1> hanno il flag superiore e il bocconcino di dimensioni inferiori. Il flag indica se l'handle viene passato da un puntatore. Il campo dimensione fornisce le dimensioni del tipo di handle generico definito dall'utente. Questa dimensione è limitata a 1, 2 o 4 byte nei sistemi a 32 bit e 1, 2, 4 o 8 byte nei sistemi a 64 bit.

Il campo Offset<2> fornisce l'offset dall'inizio dello stack del puntatore ai dati delle dimensioni specificate.

L' \_ \_ Indice pair di routine di associazione \_<1> campo fornisce l'indice nel campo AGenericBindingRoutinePairs del descrittore Stub ai puntatori a funzione di routine **Bind** e **UNBIND** per l'handle generico.

> [!Note]  
> Una descrizione di handle generica nel formato del tipo è la descrizione solo del tipo di dati correlato.

 

Context

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

I flag<1> indicano il modo in cui viene passato l'handle e il tipo. I flag validi sono riportati nella tabella seguente.



| Hex | Contrassegno                                   |
|-----|----------------------------------------|
| 80  | il \_ parametro handle \_ è \_ tramite \_ ptr            |
| 40  | il \_ parametro handle \_ è \_ in                  |
| 20  | il \_ parametro handle \_ è \_ out                 |
| 21  | il \_ parametro handle \_ viene \_ restituito              |
| 08  | \_handle di \_ contesto RIGOROSo NDR \_           |
| 04  | \_handle di contesto NDR \_ \_ senza \_ serializzazione    |
| 02  | \_ \_ serializzazione handle di contesto NDR \_        |
| 01  | l' \_ handle del contesto NDR \_ \_ non può \_ essere \_ null |



 

I primi quattro flag sono sempre presenti, le ultime quattro sono state aggiunte in Windows 2000.

Il campo Offset<2> fornisce l'offset dall'inizio dello stack all'handle di contesto.

L' \_ \_ indice di routine rundown del contesto \_<1> fornisce un indice nel campo **apfnNdrRundownRoutines** del descrittore dello stub alla routine di rundown utilizzata per questo handle di contesto. Il compilatore genera sempre un indice. Per routine che non dispongono di una routine di rundown, questo è un indice di una posizione della tabella che contiene null.

Per gli stub compilati in **-Oi2**, il parametro \_ num<1> fornisce il numero ordinale, a partire da zero, che specifica quale handle del contesto si trova nella procedura specificata.

Per le versioni precedenti dell'interprete, il param \_ num<1> fornisce il numero di parametro dell'handle di contesto, a partire da zero, nella relativa procedura.

> [!Note]  
> Una descrizione dell'handle di contesto nella stringa di formato del tipo non avrà l'offset<2> nella descrizione.

 

## <a name="the-new-oif-header"></a>Nuova intestazione – OIF

Come indicato in precedenza, l'intestazione [**-OIF**](/windows/desktop/Midl/-oi) si espande sull'intestazione **-OI** . Per praticità, vengono visualizzati tutti i campi:

(Intestazione precedente)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(Estensioni [**-OIF**](/windows/desktop/Midl/-oi) )

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

La costante \_ \_ \_ dimensione del buffer client<2> fornisce le dimensioni del buffer di marshalling che potrebbero essere state pre-calcolate dal compilatore. Può trattarsi solo di una dimensione parziale, perché il flag ClientMustSize attiva il ridimensionamento.

La \_ dimensione del buffer del server costante \_ \_<2> fornisce le dimensioni del buffer di marshalling come pre-calcolato dal compilatore. Può trattarsi solo di una dimensione parziale, perché il flag ServerMustSize attiva il ridimensionamento.

I \_ flag di consenso esplicito dell'interprete \_ sono definiti in Ndrtypes. h:

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

-   Il bit ServerMustSize viene impostato se il server deve eseguire un passaggio di ridimensionamento del buffer.
-   Il bit ClientMustSize viene impostato se il client deve eseguire un passaggio di ridimensionamento del buffer.
-   Il bit HasReturn viene impostato se la routine ha un valore restituito.
-   Il bit HasPipes viene impostato se il pacchetto pipe deve essere utilizzato per supportare un argomento pipe.
-   Il bit HasAsyncUuid viene impostato se la procedura è una procedura DCOM asincrona.
-   Il bit HasExtensions indica che vengono utilizzate le estensioni Windows 2000 e successive.
-   Il bit HasAsyncHandle indica una procedura RPC asincrona.

Il bit HasAsyncHandle è stato inizialmente usato per un'implementazione DCOM diversa del supporto asincrono e pertanto non può essere usato per il supporto asincrono dello stile corrente in DCOM. Il bit HasAsyncUuid attualmente indica questo.

 

 