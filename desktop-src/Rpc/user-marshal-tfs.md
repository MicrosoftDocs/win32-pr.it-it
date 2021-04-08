---
title: Marshalling utente
description: Marshalling utente in RPC (Remote Procedure Call).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856141"
---
# <a name="user-marshal"></a>Marshalling utente

Il marshalling dell'utente ha una stringa di formato simile a trasmissione \_ come:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

I flag<1> byte sono costituiti dal contrassegno superiore e dal bocconcino di allineamento inferiore.

I 2 bit superiori del contrassegno sono usati per descrivere se il tipo di Wire è definito come puntatore univoco, puntatore di riferimento o nessun puntatore (non può essere un PTR). Per impostare o ottenere i flag, sono stati definiti i manifesti seguenti:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

Il bocconcino di allineamento della parola del flag mantiene l'allineamento del conduttore del tipo trasmesso.

L'indice quadruplo \_<2> è un indice della routine di callback quadrupla delle funzioni di marshalling degli utenti. Le posizioni di routine sono le seguenti: ridimensionamento, marshalling, unmarshalling e liberazione di routine.

La \_ dimensione della memoria del tipo di utente \_ \_<2> fornisce una dimensione per il tipo specifico dell'utente, inclusi i tipi sconosciuti.

Le \_ dimensioni del buffer dei tipi trasmessi \_ \_<2> sono pari a zero quando la dimensione è variabile o alle dimensioni fisse effettive. Si tratta di un'ottimizzazione che consente a MIDL di ignorare i callback durante il ridimensionamento del buffer e anche quando viene liberato.

## <a name="range"></a>Range

Il \[ controllo dell'intervallo \] fornisce metodi aggiuntivi per la convalida degli argomenti a livello di rapporto di recapito. Il \[ \] descrittore di intervallo presenta il formato seguente:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

I flag accettano il bocconcino superiore e il tipo il bocconcino inferiore del secondo byte. I valori bassi e alti dipendono dal tipo della variabile da verificare.

I flag sono intesi come veicoli di espansione. il compilatore ha impostato il bocconcino su zero.

 

 




