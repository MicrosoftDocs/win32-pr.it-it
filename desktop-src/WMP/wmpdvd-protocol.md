---
title: Protocollo WMPDVD
description: Protocollo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolli
- Modello a oggetti di Windows Media Player, protocolli
- modello a oggetti, protocolli
- Controllo ActiveX di Windows Media Player, protocolli per il modello a oggetti
- Controllo ActiveX, protocolli per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, protocolli per il modello a oggetti
- Windows Media Player Mobile, protocolli per il modello a oggetti
- protocolli, modello a oggetti di Windows Media Player
- protocolli, WMPDVD
- Protocollo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329663"
---
# <a name="wmpdvd-protocol"></a>Protocollo WMPDVD

Il protocollo WMPDVD consente di specificare un supporto da un DVD usando la sintassi dell'URL. Questo è il formato generale del protocollo:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



Il segmento *unità* è la lettera dell'unità DVD; non include i due punti usati in genere con gli identificatori di unità. Questo segmento è sempre obbligatorio.

Il segmento del *titolo* è il numero del titolo da riprodurre. Non è necessario a meno che non si desideri avviare la riproduzione a un titolo specifico o a un capitolo specifico di un titolo specifico.

Il segmento del *capitolo* è il numero del capitolo da riprodurre. Non è necessario a meno che non si desideri avviare la riproduzione in un capitolo specifico di un titolo specifico.

L'argomento ContentDir e è il percorso di un VIDEO \_ TS. File IFO, che può trovarsi in una risorsa di archiviazione locale o in una condivisione di rete. Se si include questo segmento, il segmento di *unità* viene ignorato anche se è ancora necessario. Se si include anche il segmento *titolo* o i segmenti *titolo* e *capitolo* , sono relativi al contenuto DVD specificato nel segmento ContentDir e, non al segmento di *unità* .

Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre il DVD dall'inizio, come se si stesse avviando automaticamente.


```C++
player.url = "wmpdvd://F";
```



Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre il DVD dall'inizio del titolo specificato.


```C++
player.url = "wmpdvd://F/2";
```



Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre il DVD dal capitolo specificato.


```C++
player.url = "wmpdvd://F/2/4";
```



Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre contenuto DVD dalla risorsa di archiviazione locale. La stringa di *percorso* termina con la cartella che contiene il video \_ TS. File IFO; non include il nome del file. In questo esempio, il valore del segmento di *unità* non ha alcun effetto anche se è obbligatorio e la riproduzione inizia nel capitolo 4 del titolo 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



Per l'assegnazione di una stringa WMPDVD alla proprietà **URL** è necessario Windows Media Player 9 Series o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Protocolli e tipi di file supportati**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




