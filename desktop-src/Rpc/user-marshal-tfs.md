---
title: Marshalling dell'utente
description: Marshalling utente in RPC (Remote Procedure Call).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dcc9574b49a46b6e867fc4bca314944589ccf68b9d6e3fb8695a099eb255c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010848"
---
# <a name="user-marshal"></a>Marshalling dell'utente

Il marshalling utente ha una stringa di formato simile a trasmetti \_ come:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

I flag<1> byte sono costituiti dal nibble del flag superiore e dal nibble di allineamento inferiore.

I 2 bit superiori del flag nibble vengono usati per descrivere se il tipo di collegamento è definito come puntatore univoco, puntatore di riferimento o nessun puntatore (non può essere un ptr). I manifesti seguenti sono stati definiti per impostare/ottenere i flag:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

Il nibble di allineamento della parola flag mantiene l'allineamento del cavo del tipo trasmesso.

L'indice quadruplo<2> è un indice della \_ routine di callback quadrupla delle funzioni di marshalling utente. Le posizioni di routine sono le seguenti: ridimensionamento, marshalling, annullamento del marshalling e routine di liberatura.

Le dimensioni della memoria<tipo utente<2> una dimensione per il tipo specifico dell'utente, \_ \_ inclusi i tipi \_ sconosciuti.

La dimensione del buffer del tipo trasmesso<2> è zero quando le dimensioni sono variabili \_ \_ o le dimensioni \_ fisse effettive. Si tratta di un'ottimizzazione che consente a MIDL di ignorare i callback durante il ridimensionamento del buffer e anche durante la liberatura.

## <a name="range"></a>Intervallo

Il \[ controllo \] dell'intervallo offre altri mezzi per la convalida degli argomenti a livello di rapporto di mancato recapito. Il \[ formato \] del descrittore di intervallo è il seguente:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

I flag accettano il nibble superiore e il tipo il nibble inferiore del secondo byte. I valori minimo e alto dipendono dal tipo di variabile da controllare.

I flag sono pensati come veicolo di espansione. il compilatore ha impostato nibble su zero.

 

 




