---
title: Unioni RPC
description: Unioni incapsulate e non incapsulate e relativo formato con RPC (Remote Procedure Call).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473163"
---
# <a name="rpc-unions"></a>Unioni RPC

Sia le unioni incapsulate che quelle non incapsulate condividono un \_ selettore di Unione ARM comune \_<> formato:

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Il \_ campo Union arms<2> è costituito da due parti. Se l'Unione è un'Unione di stile MIDL 1,0, i 4 bit superiori contengono l'allineamento del ARM di Unione (allineamento del braccio allineato più grande). In caso contrario, i 4 bit superiori sono pari a zero. I 12 bit inferiori contengono il numero di bracci nell'Unione. In altre parole:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

La descrizione dell'offset \_ a \_ ARM \_<2> i campi contengono un offset con segno relativo alla descrizione del tipo del ARM. Tuttavia, il campo è sovraccarico con ottimizzazione per i tipi semplici. Per questi, il byte superiore di questo campo offset è FC \_ Magic \_ Union \_ byte (0x80) e il byte più basso di short è il tipo di carattere di formato effettivo del ARM. Di conseguenza, sono disponibili due intervalli per i valori di offset: "80 *XX*" significa che *XX* è una stringa di formato del tipo. e tutto il resto entro l'intervallo (80 FF... 7F FF) indica un offset effettivo. Questa operazione rende gli offset dall'intervallo <80 00. 80 FF non > disponibili come offset. Il compilatore verifica che a partire da MIDL versione 5.1.164.

Il \_ campo Default ARM \_ Description<2> indica il tipo di ARM Union per l'ARM predefinito, se disponibile. Se non è specificato un ARM predefinito per l'Unione, la descrizione predefinita di \_ arm \_<2> campo è 0xFFFF e viene generata un'eccezione se il \_ valore dell'opzione non corrisponde ad alcuno dei valori del case ARM. Se il ARM predefinito è specificato ma vuoto, il campo Default \_ ARM \_ Description<2> è zero. In caso contrario \_ , il campo Default ARM \_ Description<2> ha la stessa semantica dell'offset \_ a \_ arm \_ Description<2> Fields.

Di seguito è riportato un riepilogo:

-   0: valore predefinito vuoto
-   FFFF-nessun valore predefinito
-   80xx-tipo semplice
-   altro offset relativo

## <a name="encapsulated-unions"></a>Unioni incapsulate

Un'Unione incapsulata deriva da una speciale sintassi di Unione in IDL. In realtà, un'Unione incapsulata è una struttura di aggregazione con un campo discriminante all'inizio della struttura e l'Unione come unico altro membro.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

Il tipo di opzione di un'Unione incapsulata \_<1> campo è costituito da due parti. Il morso inferiore fornisce il tipo di Commuter effettivo e il bocconcino superiore fornisce l'incremento della memoria per eseguire un'istruzione/routine che indica che il puntatore di memoria deve essere incrementato per saltare oltre l'opzione \_ è Field, che include la spaziatura interna tra il \_ campo switch is () della struttura costruita dallo stub e il campo Union effettivo.

Le \_ dimensioni della memoria<2> campo sono solo le dimensioni dell'Unione ed è identica alle unioni non incapsulate. Per ottenere la dimensione totale della struttura che contiene l'Unione, aggiungere la dimensione della memoria \_<2> all'incremento della memoria per eseguire un'istruzione/routine, ovvero al morso superiore del tipo di commutere \_<1 campo> e quindi allinearlo in base all'allineamento corrispondente all'incremento.

## <a name="nonencapsulated-unions"></a>Unioni non incapsulate

Un'Unione non incapsulata è una situazione tipica in cui un'Unione è un argomento o un campo e l'opzione è un altro argomento o campo, rispettivamente.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Dove:

Il \_ tipo di opzione<1> campo è un carattere di formato per discriminante.

L'opzione \_ è \_ descrittore<> campo è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) . Tuttavia, per l'opzione \_ è \_ Description<>, se l'Unione è incorporata in una struttura, il campo offset dell'opzione \_ è \_ Description<> è l'offset per l'opzione \_ è il campo dalla posizione dell'Unione nella struttura (non dall'inizio della struttura).

Il \_ campo offset \_ per \_ size \_ e \_ Descrizione ARM<2> fornisce l'offset alle dimensioni dell'Unione e alla descrizione ARM, che è identica a quella per le unioni incapsulate e viene condivisa da tutte le unioni non incapsulate dello stesso tipo:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 