---
description: "Altre informazioni su: ricerca di record nell'indice"
title: Ricerca di record nell'indice
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313075"
---
# <a name="searching-records-in-the-index"></a>Ricerca di record nell'indice


_**Si applica a:** Windows | Windows Server_

## <a name="searching-records-in-the-index"></a>Ricerca di record nell'indice

Vengono create chiavi di ricerca per cercare una singola voce o un set di voci in un indice. I tasti di ricerca possono essere costruiti solo per le colonne chiave dell'indice e possono contenere uno o più valori di colonna. La chiave di ricerca viene costruita con una singola chiamata o una serie di chiamate a [JetMakeKey](./jetmakekey-function.md)e può essere recuperata con [JetRetrieveKey](./jetretrievekey-function.md) usando JET_bitRetrieveCopy. Una volta creato, il tasto di ricerca può essere utilizzato per spostare il cursore sul record nell'indice.

Sono disponibili tre metodi per trovare i record in una tabella:

1.  Cercare una singola voce di indice. A tale scopo, creare la chiave di ricerca con [JetMakeKey](./jetmakekey-function.md)e quindi passare a tale record con [JetSeek](./jetseek-function.md).

2.  Eseguire una ricerca nell'indice record per record. I record possono essere attraversati un record alla volta chiamando [JetMove](./jetmove-function.md). È possibile spostare il cursore sul primo record nell'indice specificando JET_MoveFirst nel parametro *Crow* di [JetMove](./jetmove-function.md). Allo stesso modo, è possibile spostare il cursore avanti, indietro o fino all'ultima voce dell'indice.

3.  Eseguire una ricerca in un set di record. A tale scopo, impostare un intervallo di voci di indice in cui eseguire la ricerca, quindi spostarsi tra i record in modo sequenziale. Per ulteriori informazioni, vedere [la sezione ricerca di un set di record]() di questo argomento.

### <a name="searching-through-a-set-of-records"></a>Ricerca in un set di record

Il diagramma mostra il cursore che scorre un intervallo di voci di indice definito dalle chiamate a [JetSeek](./jetseek-function.md) e [JetSetIndexRange](./jetsetindexrange-function.md).

Utilizzare la procedura seguente per eseguire la ricerca in un set di record in un indice.

### <a name="to-search-a-set-of-records-in-an-index"></a>Per eseguire la ricerca in un set di record in un indice

1.  Creare la chiave di ricerca per il primo record nel set di record in cui eseguire la ricerca con [JetMakeKey](./jetmakekey-function.md).

2.  Spostare il cursore sul record indicato nella chiave di ricerca con [JetSeek](./jetseek-function.md).

3.  Creare un'altra chiave di ricerca per l'ultima voce di indice nell'intervallo con [JetMakeKey](./jetmakekey-function.md).

4.  Impostare l'intervallo di indici con [JetSetIndexRange](./jetsetindexrange-function.md) usando la chiave creata nel passaggio 3.

5.  Chiamare [JetMove](./jetmove-function.md) per spostarsi in sequenza attraverso ogni record nell'intervallo di indici, come illustrato nella figura seguente.

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

Il cursore del diagramma può spostarsi solo nell'intervallo di indici impostati nella chiamata a [JetSetIndexRange](./jetsetindexrange-function.md). Se l'applicazione tenta di spostare il cursore oltre l'intervallo di indici, ESE restituisce un errore Jet_errNoCurrentRecord dalla chiamata a [JetMove](./jetmove-function.md). Si noti che qualsiasi tipo di navigazione con il cursore diverso dal passaggio al record successivo o precedente annullerà l'intervallo di indici. Per ulteriori informazioni, vedere [JetSetIndexRange](./jetsetindexrange-function.md) .

Il tipo di dati immessi nel parametro *pvData* per [JetMakeKey](./jetmakekey-function.md) deve corrispondere al tipo di dati e alle proprietà specificate per la colonna. Ad esempio, la chiamata di [JetMakeKey](./jetmakekey-function.md) con "Ben Miller" specificata nel parametro *pvData* per un tipo di colonna JET_coltypText è un tipo di dati valido corrispondente. Se si vuole creare una chiave di ricerca per eseguire la ricerca tra i nomi "Ben Miller" e "Max Stevens" in un indice, spostare il cursore sul record con il nome "Ben Miller" chiamando [JetSeek](./jetseek-function.md). Chiamare [JetMakeKey](./jetmakekey-function.md) una seconda volta e specificare un puntatore a una stringa contenente il nome "Max Stevens". L'intervallo di indicizzazione è impostato in modo da limitare il passaggio del cursore tra i nomi "Ben Miller" e "Max Stevens" nella chiamata a [JetSetIndexRange](./jetsetindexrange-function.md).
