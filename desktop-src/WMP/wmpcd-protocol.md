---
title: Protocollo WMPCD
description: Protocollo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolli
- Windows Media Player a oggetti, protocolli
- modello a oggetti,protocolli
- Windows Media Player ActiveX, protocolli per il modello a oggetti
- ActiveX, protocolli per il modello a oggetti
- Windows Media Player Controllo di ActiveX per dispositivi mobili, protocolli per il modello a oggetti
- Windows Media Player Dispositivi mobili, protocolli per il modello a oggetti
- protocolli, Windows Media Player a oggetti
- protocolli, WMPCD
- Protocollo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b1359d22b792587f7cceeb46f0f9e621585dfba296422a227e9012077df7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900141"
---
# <a name="wmpcd-protocol"></a>Protocollo WMPCD

Il protocollo WMPCD consente di specificare tracce in un compact disc usando la sintassi dell'URL. Questa è la sintassi generale del protocollo:


```C++
wmpcd://drive/track
```



Il *segmento* di unità è l'indice dell'unità CD. Il *segmento* di traccia è il numero della traccia. L'esempio seguente illustra l'uso del protocollo WMPCD.


```C++
player.url = "wmpcd://0/4";
```



L'esempio riproduce la quarta traccia sul disco nella prima unità CD (l'unità il cui indice è 0).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Protocolli e tipi di file supportati**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




