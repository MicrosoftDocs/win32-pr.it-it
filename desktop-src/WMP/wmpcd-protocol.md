---
title: Protocollo WMPCD
description: Protocollo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolli
- Modello a oggetti di Windows Media Player, protocolli
- modello a oggetti, protocolli
- Controllo ActiveX di Windows Media Player, protocolli per il modello a oggetti
- Controllo ActiveX, protocolli per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, protocolli per il modello a oggetti
- Windows Media Player Mobile, protocolli per il modello a oggetti
- protocolli, modello a oggetti di Windows Media Player
- protocolli, WMPCD
- Protocollo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221379"
---
# <a name="wmpcd-protocol"></a>Protocollo WMPCD

Il protocollo WMPCD consente di specificare tracce in un disco Compact usando la sintassi dell'URL. Questa è la sintassi generale del protocollo:


```C++
wmpcd://drive/track
```



Il segmento *unità* è l'indice dell'unità CD. Il segmento *Track* è il numero della traccia. Nell'esempio seguente viene illustrato l'utilizzo del protocollo WMPCD.


```C++
player.url = "wmpcd://0/4";
```



Nell'esempio viene riprodotta la quarta traccia del disco nella prima unità CD (l'unità il cui indice è 0).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Protocolli e tipi di file supportati**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




