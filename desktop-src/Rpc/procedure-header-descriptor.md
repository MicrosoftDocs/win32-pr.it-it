---
title: Descrittore di intestazioni di routine
description: L'intestazione è stata estesa più volte nel corso della durata del motore di rapporto di recapito. Il compilatore corrente genera comunque intestazioni diverse a seconda della modalità del compilatore. Tuttavia, le intestazioni più recenti sono un superset di quelle precedenti.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473902"
---
# <a name="procedure-header-descriptor"></a>Descrittore di intestazioni di routine

L'intestazione è stata estesa più volte nel corso della durata del motore di rapporto di recapito. Il compilatore corrente genera comunque intestazioni diverse a seconda della modalità del compilatore. Tuttavia, le intestazioni più recenti sono un superset di quelle precedenti.

## <a name="the-old-oi-header"></a>Intestazione-OI precedente

Il formato dell'intestazione è il seguente:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Dove \_ il tipo di handle<1> può essere uno dei valori mostrati nella tabella seguente.



| Hex | Handle               |
|-----|----------------------|
| 31  | \_associazione FC \_ generica    |
| 32  | \_ \_ primitiva bind FC  |
| 33  | \_handle automatico \_ FC     |
| 34  | \_handle di callback FC \_ |
| 0   | (handle esplicito)    |



 

Se il tipo di handle \_<1> campo è diverso da zero, la stored procedure utilizza un handle implicito del tipo indicato. Per ulteriori informazioni, vedere l'argomento [Handles](handles.md) . Se il \_ tipo di handle<1> campo è zero, l'handle utilizzato per l'associazione è uno dei parametri della procedura.

Gli handle espliciti possono essere primitivi, generici e di contesto; l'ultimo token FC è il seguente.



| Hex | Handle            |
|-----|-------------------|
| 30  | \_contesto di associazione FC \_ |



 

Per convenzione, il tipo di handle per le interfacce DCOM è la \_ gestione automatica FC \_ .

Il \_ campo OI flags<1> è una maschera a 8 bit dei flag seguenti.



| Hex | Contrassegno                         | Significato                                  |
|-----|------------------------------|------------------------------------------|
| 01  | \_Ptr completo \_ OI \_ usato          | Usa il pacchetto completo del puntatore.           |
| 02  | \_Alloc RPCSS di OI \_ \_ usato       | Usa il pacchetto di memoria RpcSs.           |
| 04  | Procedura dell' \_ oggetto OI \_             | Procedura in un'interfaccia dell'oggetto.      |
| 08  | OI \_ ha \_ RPCFLAGS            | La stored procedure contiene flag RPC diversi da zero.     |
| 10  | OI\_\*                       | Di overload.                              |
| 20  | OI\_\*                       | Di overload.                              |
| 40  | OI \_ Usa \_ le \_ nuove \_ routine init | Usa le routine di Windows NT 3.5 beta2 + init. |
| 80  |                              | Non utilizzato.                                  |



 

I flag seguenti sono in overload.



| Hex | Contrassegno                                    | Significato                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | \_viene \_ usato Encode                        | Usato solo nella selezione.                              |
| 20  | \_viene usato Decode \_                        | Usato solo nella selezione.                              |
| 10  | OI \_ ignorare \_ la \_ \_ gestione delle eccezioni degli oggetti | Non più usato (OLE precedente).                         |
| 20  | OI \_ ha un \_ comma \_ o un \_ errore                | Solo in RPC non elaborata, \[ comunicazione \_ , stato di errore \_ \] .        |
| 20  | L' \_ \_ interprete OI obj USA \_ v2 \_           | Solo in DCOM usare l'interprete [**– OIF**](/windows/desktop/Midl/-oi) . |



 

Il \_ campo dei flag rpc<4> descrive come impostare il campo **RpcFlags** della struttura [**del \_ messaggio RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) . Questo campo è presente solo se i \_ flag oi<1> campo ha \_ \_ RPCFLAGS impostato OI. Se questo campo non è presente, i flag RPC per la procedura remota sono pari a zero.

> [!Note]  
> Per ottenere prestazioni, gli interpreti asincroni hanno sempre i \_ flag rpc<4> campo.

 

Il \_ campo proc num<2> fornisce il numero di procedura della stored procedure.

La dimensione dello stack \_<2> fornisce la dimensione totale di tutti i parametri nello stack, inclusi tutti i valori di puntatore e/o valore restituito.

La descrizione dell'handle esplicito \_ \_<> campo è descritta più avanti in questo documento. Questo campo non è presente se la stored procedure utilizza un handle implicito.

 

 