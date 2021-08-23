---
title: Transmit_as e Represent_as
description: Trasmetti come e rappresentano come condividono lo stesso layout, ad eccezione del token iniziale. Il token legge FC TRANSMIT AS o FC REPRESENT AS, ma il \_ \_ codice sottostante è \_ \_ \_ \_ comune.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ada873ee6e928a08dfe1d9a93928e3b00835c9f2394bde3a5194b56cce58911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011219"
---
# <a name="transmit_as-and-represent_as"></a>\_Trasmetti come e Rappresenta \_ come

Trasmetti come e rappresentano come condividono lo stesso layout, ad eccezione del token iniziale. Il token legge FC TRANSMIT AS o FC REPRESENT AS, ma il \_ \_ codice sottostante è \_ \_ \_ \_ comune.

La descrizione ha il layout seguente:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

I flag<1> byte sono costituiti dal flag superiore nibble e dal nibble di allineamento inferiore.

Il nibble di allineamento mantiene l'allineamento del cavo del tipo trasmesso. Questa operazione è necessaria quando si ridimensiona il buffer e si usano le dimensioni del tipo trasmesse dal codice di formato.

Il flag nibble può avere i flag seguenti:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

Il flag PRESENTED TYPE IS ARRAY contrassegna una trasmissione di primo livello come argomento (o rappresenta come) come matrice di un elemento e \_ \_ valore \_ passato. [**L'interprete -Oi**](/windows/desktop/Midl/-oi) usa questo flag per eseguire un'istruzione alla volta un argomento di questo tipo (che è in realtà un puntatore nello stack, non la matrice). Anche gli altri due flag vengono usati solo negli interpreti precedenti per eseguire correttamente l'istruzione su un tipo presentato nello stack.

L'indice quintuple<2> è un indice della quintupla di routine di callback (si tratta in realtà di un \_ quadruplo) di funzioni. La tabella viene comunemente trasmessa come e rappresenta come ed esiste un mapping ovvio per la posizione delle routine, in quanto gli stessi punti di ingresso trasmettono come e rappresentano come codici. Il mapping è da \_ local => a xmit, a local => from \_ \_ \_ xmit, free \_ inst => free \_ xmit, free local => free \_ \_ inst.

La dimensione di memoria del tipo presentato<2> fornisce sempre una dimensione per il tipo \_ \_ presentato/locale, inclusa la rappresentazione sconosciuta \_ come tipi.

La dimensione del buffer del \_ \_ tipo trasmesso<2> è zero, quando la dimensione è variabile \_ o la dimensione fissa effettiva. Si tratta di un'ottimizzazione che consente di ignorare alcuni callback durante il ridimensionamento del buffer.

L'offset del tipo trasmesso<2> è il consueto offset del tipo relativo alla stringa \_ di formato del tipo \_ trasmesso.

 

 