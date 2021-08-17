---
title: Descrittore dell'intestazione della procedura
description: L'intestazione è stata estesa più volte nel corso del ciclo di vita del motore NDR. Il compilatore corrente genera comunque intestazioni diverse a seconda della modalità del compilatore. Tuttavia, le intestazioni più recenti sono un superset di quelle meno recenti.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd9572c9a29ea8477f1d06d8786d50f6abf920de140b6d1663c2431b2ad0c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927134"
---
# <a name="procedure-header-descriptor"></a>Descrittore dell'intestazione della procedura

L'intestazione è stata estesa più volte nel corso del ciclo di vita del motore NDR. Il compilatore corrente genera comunque intestazioni diverse a seconda della modalità del compilatore. Tuttavia, le intestazioni più recenti sono un superset di quelle meno recenti.

## <a name="the-old-oi-header"></a>Intestazione -Oi precedente

Il formato dell'intestazione è il seguente:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Dove il \_ tipo di handle<1> può essere uno dei valori illustrati nella tabella seguente.



| Hex | Handle               |
|-----|----------------------|
| 31  | FC \_ BIND \_ GENERIC    |
| 32  | PRIMITIVA \_ DI BINDING \_ FC  |
| 33  | HANDLE \_ AUTOMATICO \_ FC     |
| 34  | HANDLE DI \_ CALLBACK \_ FC |
| 0   | (handle esplicito)    |



 

Se il tipo di handle<1> campo è diverso da zero, la routine usa un \_ handle implicito del tipo indicato. Per altre [informazioni,](handles.md) vedere l'argomento Handle. Se il tipo di handle<1> campo è zero, l'handle usato per l'associazione è uno \_ dei parametri della procedura.

Gli handle espliciti possono essere primitivi, generici e di contesto. l'ultimo ha il token FC seguente.



| Hex | Handle            |
|-----|-------------------|
| 30  | CONTESTO \_ DI BINDING \_ FC |



 

Per convenzione, il tipo di handle per le interfacce DCOM è FC \_ AUTO \_ HANDLE.

I flag Oi<1> campo è una maschera \_ a 8 bit dei flag seguenti.



| Hex | Contrassegno                         | Significato                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Oi \_ FULL \_ PTR \_ USED          | Usa il pacchetto puntatore completo.           |
| 02  | Oi \_ RPCSS \_ ALLOC \_ USED       | Usa il pacchetto di memoria RpcSs.           |
| 04  | Oi \_ OBJECT \_ PROC             | Routine in un'interfaccia a oggetti.      |
| 08  | Oi \_ HAS \_ RPCFLAGS            | La procedura ha flag Rpc diversi da zero.     |
| 10  | Oi\_\*                       | Di overload.                              |
| 20  | Oi\_\*                       | Di overload.                              |
| 40  | Oi \_ USE \_ NEW \_ INIT \_ ROUTINES | Usa Windows routine init NT3.5 Beta2+. |
| 80  |                              | Non utilizzato.                                  |



 

I flag seguenti sono sottoposti a overload.



| Hex | Contrassegno                                    | Significato                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | VIENE USATA \_ LA CODIFICA \_                        | Usato solo nel pickling.                              |
| 20  | DECODE \_ VIENE \_ USATO                        | Usato solo nel pickling.                              |
| 10  | Oi \_ IGNORE \_ OBJECT \_ EXCEPTION \_ HANDLING | Non più usato (OLE precedente).                         |
| 20  | Oi \_ HA \_ COMM O \_ \_ FAULT                | Solo in RPC non elaborato, \[ comm \_ , stato di \_ errore \] .        |
| 20  | INTERPRETE OI \_ OBJ \_ USE \_ V2 \_           | Solo in DCOM usare [**l'interprete –Oif.**](/windows/desktop/Midl/-oi) |



 

Il campo rpc flags<4> descrive come impostare il campo \_ **RpcFlags** della [**struttura RPC \_ MESSAGE.**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) Questo campo è presente solo se i flag Oi<1> \_ Oi \_ HAD \_ RPCFLAGS è impostato. Se questo campo non è presente, i flag RPC per la procedura remota sono pari a zero.

> [!Note]  
> Per le prestazioni, gli interpreti asincroni hanno sempre i flag rpc \_<4> campo.

 

Il campo \_ proc num<2> fornisce il numero di procedura della procedura.

La dimensione dello stack<2> fornisce la dimensione totale di tutti i parametri nello stack, incluso qualsiasi puntatore \_ this e/o valore restituito.

La \_ descrizione \_ esplicita dell'handle<> campo è descritta più avanti in questo documento. Questo campo non è presente se la routine usa un handle implicito.

 

 