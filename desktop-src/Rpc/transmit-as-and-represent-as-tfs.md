---
title: Transmit_as e Represent_as
description: Trasmettere \_ come e rappresentare \_ come condividono lo stesso layout ad eccezione del token principale. il token legge la \_ trasmissione FC \_ come o FC \_ rappresenta \_ come, ma il codice sottostante è comune.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963124"
---
# <a name="transmit_as-and-represent_as"></a>Trasmettere \_ come e rappresentare \_ come

Trasmettere \_ come e rappresentare \_ come condividono lo stesso layout ad eccezione del token principale. il token legge la \_ trasmissione FC \_ come o FC \_ rappresenta \_ come, ma il codice sottostante è comune.

Il layout della descrizione è il seguente:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

I flag<1> byte sono costituiti dal contrassegno superiore e dal bocconcino di allineamento inferiore.

Il bocconcino di allineamento mantiene l'allineamento del tipo trasmesso. Questa operazione è necessaria in caso di ridimensionamento del buffer e di utilizzo della dimensione del tipo trasmesso dal codice del formato.

Il flag rosicchia può includere i flag seguenti:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

Il \_ tipo presentato \_ è \_ flag di matrice contrassegna un argomento di trasmissione di primo livello (o rappresenta come) come una matrice di elementi e un valore passato per. L'interprete [**-OI**](/windows/desktop/Midl/-oi) usa questo flag per eseguire un'istruzione/routine di questo tipo (che è in realtà un puntatore sullo stack, non sulla matrice). Gli altri due flag vengono usati anche solo negli interpreti precedenti per eseguire correttamente il passaggio a un tipo presentato nello stack.

L' \_ Indice quintupla<2> è un indice della routine di callback Quintupla (si tratta in realtà di una quadrupla) di funzioni. La tabella è comune sia per trasmettere come che per rappresentare come ed esiste un mapping ovvio per la posizione delle routine, in quanto lo stesso servizio punti di ingresso trasmette e rappresenta come codici. Il mapping è da \_ local => a \_ Xmit, a \_ local => from \_ Xmit, Free \_ inst => Free \_ Xmit, Free \_ local => Free \_ inst.

La \_ \_ dimensione di memoria del tipo presentata \_<2> fornisce sempre una dimensione per il tipo presentato/locale, inclusi quelli sconosciuti come tipi.

Le \_ dimensioni del buffer dei tipi trasmessi \_ \_<2> sono pari a zero, quando le dimensioni sono variabili o le dimensioni fisse effettive. Si tratta di un'ottimizzazione che consente di ignorare alcuni callback durante il ridimensionamento del buffer.

L' \_ offset del tipo trasmesso \_<2> è il consueto offset del tipo relativo alla stringa di formato del tipo trasmesso.

 

 