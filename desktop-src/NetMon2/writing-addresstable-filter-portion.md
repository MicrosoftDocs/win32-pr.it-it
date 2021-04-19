---
description: Il filtro indirizzi invia una notifica al driver Network Monitor per accettare i frame con una varietà di tipi di indirizzi MAC specificati (Ethernet, token ring e FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Scrittura della parte di filtro ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317748"
---
# <a name="writing-addresstable-filter-portion"></a>Scrittura della parte di filtro ADDRESSTABLE

Il filtro indirizzi invia una notifica al driver Network Monitor per accettare i frame con una varietà di tipi di indirizzi MAC specificati (Ethernet, token ring e FDDI). È possibile specificare un massimo di otto coppie di indirizzi. Una coppia di indirizzi può specificare un'origine, una destinazione, entrambe o nessuna delle due.

La parte relativa all'indirizzo del filtro è costituita da due strutture: [**ADDRESSTABLE**](addresstable.md) e [**ADDRESSPAIR**](addresspair.md).

Se non si specifica alcun indirizzo, tutti i frame passeranno il filtro degli indirizzi. Tuttavia, se si specificano indirizzi, verranno superati solo i frame che passano il filtro di indirizzi specificato.

La compilazione del filtro degli indirizzi comporta l'allocazione di una struttura [**ADDRESSTABLE**](addresstable.md) e la compilazione di membri della struttura [**ADDRESSPAIR**](addresspair.md) .

**Per compilare la parte relativa all'indirizzo di un filtro di acquisizione**

1.  Usare il flag **capturefilter \_ flags \_ Local \_ only** della struttura [**capturefilter**](capturefilter.md) per limitare l'acquisizione al traffico da e verso il computer locale.

    Impostando questo flag, la scheda di interfaccia di rete non verrà impostata su modalità promiscua; il file di acquisizione acquisirà solo il traffico locale.

2.  Usare il codice di esempio seguente per definire la struttura [**ADDRESSTABLE**](addresstable.md) :

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  Usare le informazioni elencate nella tabella seguente per selezionare un tipo di flag [**ADDRESSPAIR**](addresspair.md) . 

    | Contrassegno                             | Significato                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | flag di indirizzo \_ \_ corrispondenti all' \_ ora legale       | Corrisponde a un indirizzo di destinazione.                                                        |
    | flag di indirizzo \_ \_ corrispondenti a \_ src       | Corrisponde a un indirizzo di origine                                                              |
    | \_Escludi flag di indirizzo \_          | Esclude il frame se l'indirizzo viene trovato, ovvero un'origine o una destinazione definita. |
    | INDIRIZZI \_ flag \_ del \_ gruppo \_ di indirizzi DST | Corrisponde al bit del gruppo (dell'indirizzo di destinazione) solo per i messaggi di tipo broadcast.      |
    | i \_ flag di indirizzo \_ corrispondono a \_ entrambi      | Corrisponde a entrambi gli indirizzi di destinazione e di origine.                                    |

    

     

4.  Compilare un indirizzo di destinazione, che viene valutato rispetto al flag [**ADDRESSPAIR**](addresspair.md) selezionato.
5.  Compilare un indirizzo di origine, che viene valutato rispetto al flag [**ADDRESSPAIR**](addresspair.md) selezionato.
6.  Popolare la struttura [**ADDRESSTABLE**](addresstable.md) con una matrice di strutture [**ADDRESSPAIR**](addresspair.md) , che include le coppie di indirizzi valutate dal driver. Tutte le coppie di indirizzi vengono valutate come un'istruzione OR logica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). È possibile includere un massimo di otto coppie di indirizzi in un filtro di acquisizione.

 

 



