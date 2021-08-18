---
title: Unioni RPC
description: Unioni incapsulate e non incapsulate e relativo formato con RPC (Remote Procedure Call).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5948a0557ea968a385324244d569d3578ec5d6c0dec4af5261866ed3ba2dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011019"
---
# <a name="rpc-unions"></a>Unioni RPC

Sia le unioni incapsulate che le unioni non incapsulate condividono un selettore di arm di unione comune \_ \_<> formato:

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Il campo \_ union arms<2> è costituito da due parti. Se l'unione è un'unione di stile MIDL 1.0, i 4 bit superiori contengono l'allineamento del braccio dell'unione (allineamento del braccio allineato più grande). In caso contrario, i 4 bit superiori sono zero. I 12 bit inferiori contengono il numero di bracci nell'unione. In altre parole:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

La descrizione dell'offset<2> contiene un offset con segno relativo rispetto \_ \_ alla \_ descrizione del tipo del arm. Tuttavia, il campo viene sottoposto a overload con l'ottimizzazione per i tipi semplici. Per questi valori, il byte superiore di questo campo di offset è FC \_ MAGIC \_ UNION BYTE (0x80) e il byte inferiore di short è il tipo di carattere di formato effettivo \_ del arm. Di conseguenza, esistono due intervalli per i valori di offset: "80 *xx"* indica che *xx* è una stringa di formato del tipo. e tutto il resto entro l'intervallo (80 FF .. 7f FF) indica un offset effettivo. Questo rende gli offset dall'intervallo <80 00 .. 80 FF > non disponibile come offset. Il compilatore lo verifica a a livello di MIDL versione 5.1.164.

La descrizione predefinita del<2> campo indica il tipo di arm di unione per il arm \_ \_ predefinito, se presente. Se non è stato specificato alcun arm predefinito per l'unione, il campo predefinito arm description<2> è 0xFFFF e viene generata un'eccezione se l'opzione è value non corrisponde a nessuno dei valori del case \_ \_ \_ arm. Se il arm predefinito è specificato ma vuoto, la descrizione predefinita del<2> \_ campo è \_ zero. In caso contrario, la descrizione predefinita del<2> ha la stessa semantica dell'offset per la descrizione del<2> \_ \_ \_ \_ \_ campo.

Di seguito è riportato un riepilogo:

-   0 - valore predefinito vuoto
-   FFFF : nessuna impostazione predefinita
-   80xx - tipo semplice
-   other - offset relativo

## <a name="encapsulated-unions"></a>Unioni incapsulate

Un'unione incapsulata deriva da una sintassi di unione speciale in IDL. In effetti, un'unione incapsulata è una struttura di aggregazione con un campo discriminante all'inizio della struttura e l'unione come unico altro membro.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

Il tipo di commutatore di \_ un'unione incapsulata<1> campo è in due parti. Il nibble inferiore fornisce il tipo di commutatore effettivo e il nibble superiore fornisce l'incremento di memoria per il passaggio, ovvero una quantità che il puntatore alla memoria deve essere incrementato per ignorare l'opzione è field, che include qualsiasi riempimento tra il campo switch is() della struttura costruita con stub e il campo \_ \_ di unione effettivo.

Le dimensioni della<2> campo sono solo le dimensioni dell'unione ed è identica alle \_ unioni non incapsulate. Per ottenere le dimensioni totali della struttura che contiene l'unione, aggiungere le dimensioni della memoria<2> all'incremento della memoria per eseguire il passaggio, cio? al valore superiore del campo switch type<1> e quindi allinearlo in base all'allineamento corrispondente \_ \_ all'incremento.

## <a name="nonencapsulated-unions"></a>Unioni non incapsulate

Un'unione non incapsulata è una situazione tipica in cui un'unione è un argomento o un campo e l'opzione è rispettivamente un altro argomento o campo.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Dove:

Il tipo \_ di<1> è un carattere di formato per la discriminante.

L'opzione è il<> campo è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno usato. Tuttavia, per l'opzione è descrizione<>, se l'unione è incorporata in una struttura, il campo offset dell'opzione è descrizione<> è l'offset dell'opzione è campo dalla posizione dell'unione nella struttura \_ \_ \_ \_ \_ (non dall'inizio della struttura).

L'offset per le dimensioni e la descrizione del braccio<2> assegna l'offset alle dimensioni e alla descrizione del braccio \_ \_ \_ \_ dell'unione, che è identico a quello per le unioni incapsulate ed è condiviso da tutte le unioni non incapsulate dello \_ stesso tipo:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 