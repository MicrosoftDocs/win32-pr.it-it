---
title: Protocollo WMPDVD
description: Protocollo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolli
- Windows Media Player a oggetti, protocolli
- modello a oggetti,protocolli
- Windows Media Player ActiveX, protocolli per il modello a oggetti
- ActiveX, protocolli per il modello a oggetti
- Windows Media Player Controllo di ActiveX per dispositivi mobili, protocolli per il modello a oggetti
- Windows Media Player Dispositivi mobili, protocolli per il modello a oggetti
- protocolli, Windows Media Player a oggetti
- protocolli, WMPDVD
- Protocollo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca67f3cdee6f040aeb266e02493425ca76715ade2e3269f4377ba340af89cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761291"
---
# <a name="wmpdvd-protocol"></a>Protocollo WMPDVD

Il protocollo WMPDVD consente di specificare supporti da un DVD usando la sintassi dell'URL. Questa è la forma generale del protocollo:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



Il *segmento* di unità è la lettera dell'unità DVD; non include i due punti usati in genere con gli identificatori di unità. Questo segmento è sempre obbligatorio.

Il *segmento* del titolo è il numero del titolo da riprodurre. Non è necessario a meno che non si voglia avviare la riproduzione in corrispondenza di un titolo specifico o di un capitolo specifico di un titolo specifico.

Il *segmento* del capitolo è il numero del capitolo da riprodurre. Non è necessario a meno che non si voglia avviare la riproduzione in un capitolo specifico di un titolo specifico.

L'argomento contentdir è il percorso di un video \_ TS. File IFO, che può essere in una risorsa di archiviazione locale o in una condivisione di rete. Se si include questo segmento, il segmento di *unità* viene ignorato anche se è ancora obbligatorio. Se si include anche *il*  segmento  del titolo o entrambi i segmenti titolo e capitolo, questi sono relativi al contenuto del DVD specificato nel segmento contentdir, non al segmento *di* unità.

Nell'esempio seguente viene utilizzato il protocollo WMPDVD per riprodurre il DVD dall'inizio, come se si avviava automaticamente.


```C++
player.url = "wmpdvd://F";
```



Nell'esempio seguente viene utilizzato il protocollo WMPDVD per riprodurre il DVD dall'inizio del titolo specificato.


```C++
player.url = "wmpdvd://F/2";
```



Nell'esempio seguente viene utilizzato il protocollo WMPDVD per riprodurre il DVD dal capitolo specificato.


```C++
player.url = "wmpdvd://F/2/4";
```



Nell'esempio seguente viene utilizzato il protocollo WMPDVD per riprodurre contenuto DVD dall'archiviazione locale. La *stringa* di percorso termina con la cartella che contiene video \_ TS. File IFO; non include il nome del file. In questo esempio, il valore del *segmento* di unità non ha alcun effetto anche se è obbligatorio e la riproduzione inizia nel capitolo 4 del titolo 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



L'assegnazione di una stringa WMPDVD alla proprietà **url** Windows Media Player serie 9 o successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Protocolli e tipi di file supportati**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




