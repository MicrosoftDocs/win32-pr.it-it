---
description: Il filtro indirizzi notifica al driver Network Monitor accettare frame con uno dei diversi tipi di indirizzi MAC specificati (Ethernet, Token Ring e FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Scrittura della parte di filtro ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a18f8004ea4c38607d6c1c7b8fa741315b41fefe5b4d31b103167d415eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128791"
---
# <a name="writing-addresstable-filter-portion"></a>Scrittura della parte di filtro ADDRESSTABLE

Il filtro indirizzi notifica al driver Network Monitor accettare frame con uno dei diversi tipi di indirizzi MAC specificati (Ethernet, Token Ring e FDDI). È possibile specificare un massimo di otto coppie di indirizzi. Una coppia di indirizzi può specificare un'origine, una destinazione, entrambe o nessuna delle due.

La parte relativa all'indirizzo del filtro è costituita da due strutture: [**ADDRESSTABLE**](addresstable.md) [**e ADDRESSPAIR.**](addresspair.md)

Se si specifica NO addresses, TUTTI i frame passeranno il filtro degli indirizzi. Tuttavia, se si specificano indirizzi, verranno passati solo i frame che superano il filtro di indirizzi specificato.

La compilazione del filtro indirizzi comporta l'allocazione [**di una struttura ADDRESSTABLE**](addresstable.md) e la compilazione dei membri [**della struttura ADDRESSPAIR.**](addresspair.md)

**Per compilare la parte dell'indirizzo di un filtro di acquisizione**

1.  Usare il flag **CAPTUREFILTER \_ FLAGS LOCAL \_ \_ ONLY** della struttura [**CAPTUREFILTER**](capturefilter.md) per limitare l'acquisizione al traffico da e verso il computer locale.

    L'impostazione di questo flag non imposta la scheda di interfaccia di rete sulla modalità promiscua. Il file di acquisizione acquisisce solo il traffico locale.

2.  Usare il codice di esempio seguente per definire la [**struttura ADDRESSTABLE:**](addresstable.md)

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

3.  Usare le informazioni elencate nella tabella seguente per selezionare un tipo di flag [**ADDRESSPAIR.**](addresspair.md) 

    | Contrassegno                             | Significato                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | FLAG DI \_ INDIRIZZO \_ CORRISPONDENTI \_ ALL'ORA LEGALE       | Corrisponde a un indirizzo di destinazione.                                                        |
    | I FLAG \_ DI \_ INDIRIZZO CORRISPONDONO A \_ SRC       | Corrisponde a un indirizzo di origine                                                              |
    | FLAG DI \_ INDIRIZZO \_ ESCLUDI          | Esclude il frame se questo indirizzo viene trovato (origine o destinazione definita). |
    | ADDR \_ \_ DEL GRUPPO DST DEI FLAG \_ DI \_ INDIRIZZO | Corrisponde al bit di gruppo (dell'indirizzo di destinazione) solo per i messaggi di tipo broadcast.      |
    | I FLAG \_ DI INDIRIZZO \_ CORRISPONDONO A \_ ENTRAMBI      | Corrisponde agli indirizzi di destinazione e di origine.                                    |

    

     

4.  Compilare un indirizzo di destinazione, che viene valutato rispetto al flag [**ADDRESSPAIR**](addresspair.md) selezionato.
5.  Compilare un indirizzo di origine, che viene valutato rispetto al flag [**ADDRESSPAIR**](addresspair.md) selezionato.
6.  Popolare la struttura [**ADDRESSTABLE**](addresstable.md) con una matrice di [**strutture ADDRESSPAIR,**](addresspair.md) che include le coppie di indirizzi valutate dal driver. Tutte le coppie di indirizzi vengono valutate come istruzione OR logica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). È possibile includere un massimo di otto coppie di indirizzi in un filtro di acquisizione.

 

 



