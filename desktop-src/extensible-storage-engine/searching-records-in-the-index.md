---
description: "Altre informazioni su: Ricerca di record nell'indice"
title: Ricerca di record nell'indice
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 57b8229c7f243c4a20bc3cd22cf285d58993a6371efc14620fe98bb8bf4620af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703111"
---
# <a name="searching-records-in-the-index"></a>Ricerca di record nell'indice


_**Si applica a:** Windows | Windows Server_

## <a name="searching-records-in-the-index"></a>Ricerca di record nell'indice

Le chiavi di ricerca vengono create per cercare una singola voce o un set di voci in un indice. Le chiavi di ricerca possono essere costruite solo per le colonne chiave nell'indice e possono contenere uno o più valori di colonna. La chiave di ricerca viene costruita con una singola chiamata o una serie di chiamate a [JetMakeKey](./jetmakekey-function.md)e può essere recuperata con [JetRetrieveKey](./jetretrievekey-function.md) usando JET_bitRetrieveCopy. Dopo la costruzione, la chiave di ricerca può essere usata per spostare il cursore sul record nell'indice.

Esistono tre metodi per trovare i record in una tabella:

1.  Cercare una singola voce di indice. A tale scopo, creare la chiave di ricerca [con JetMakeKey](./jetmakekey-function.md)e quindi passare a tale record [con JetSeek](./jetseek-function.md).

2.  Cercare il record dell'indice in base al record. I record possono essere attraversati un record alla volta chiamando [JetMove](./jetmove-function.md). Il cursore può essere spostato nel primo record dell'indice specificando JET_MoveFirst nel parametro *cRow* di [JetMove](./jetmove-function.md). Allo stesso modo, il cursore può essere spostato in avanti, all'indietro o all'ultima voce nell'indice.

3.  Eseguire una ricerca in un set di record. A tale scopo, impostare un intervallo di voci di indice in cui eseguire la ricerca, quindi spostarsi tra i record in sequenza. Per altre informazioni, vedere [la sezione Ricerca di un set]() di record in questo argomento.

### <a name="searching-through-a-set-of-records"></a>Ricerca in un set di record

Il diagramma seguente illustra lo spostamento del cursore in un intervallo di voci di indice definito dalle chiamate a [JetSeek](./jetseek-function.md) [e JetSetIndexRange.](./jetsetindexrange-function.md)

Usare la procedura seguente per eseguire la ricerca in un set di record in un indice.

### <a name="to-search-a-set-of-records-in-an-index"></a>Per cercare un set di record in un indice

1.  Creare la chiave di ricerca per il primo record nel set di record in cui eseguire la ricerca con [JetMakeKey](./jetmakekey-function.md).

2.  Spostare il cursore sul record indicato nella chiave di ricerca con [JetSeek](./jetseek-function.md).

3.  Creare un'altra chiave di ricerca per l'ultima voce di indice nell'intervallo con [JetMakeKey](./jetmakekey-function.md).

4.  Impostare l'intervallo di indici [con JetSetIndexRange](./jetsetindexrange-function.md) usando la chiave creata nel passaggio 3.

5.  Chiamare [JetMove per](./jetmove-function.md) spostarsi in sequenza tra ogni record nell'intervallo di indici, come illustrato nel diagramma seguente.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

Il cursore nel diagramma può spostarsi solo nell'intervallo di indici impostato nella chiamata a [JetSetIndexRange.](./jetsetindexrange-function.md) Se l'applicazione tenta di spostare il cursore oltre l'intervallo di indice, ESE restituisce un errore Jet_errNoCurrentRecord dalla chiamata a [JetMove](./jetmove-function.md). Si noti che qualsiasi tipo di spostamento con questo cursore diverso dal passaggio al record successivo o precedente annullerà l'intervallo di indici. Per [altre informazioni, vedere JetSetIndexRange.](./jetsetindexrange-function.md)

Il tipo di dati immessi nel *parametro pvData* per [JetMakeKey](./jetmakekey-function.md) deve corrispondere al tipo di dati e alle proprietà specificati per la colonna. Ad esempio, la chiamata di [JetMakeKey](./jetmakekey-function.md) con "Ben Miller" specificato nel parametro *pvData* per un tipo di colonna JET_coltypText corrisponde a un tipo di dati valido. Se si vuole creare una chiave di ricerca per cercare tra i nomi "Ben Miller" e "Max Stevens" in un indice, spostare il cursore sul record con il nome "Ben Miller" chiamando [JetSeek](./jetseek-function.md). Chiamare [JetMakeKey](./jetmakekey-function.md) una seconda volta e specificare un puntatore a una stringa contenente il nome "Max Stevens". L'intervallo di indici è impostato per limitare il cursore per spostarsi tra i nomi "Ben Miller" e "Max Stevens" nella chiamata a [JetSetIndexRange.](./jetsetindexrange-function.md)
