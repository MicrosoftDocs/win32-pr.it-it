---
title: Colore RGB raggiunto
description: Colore RGB raggiunto
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Windows Media Player Mobile Skins, colori pulsante
- interfacce, colori pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, colori
- riferimento ai colori per le interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298653"
---
# <a name="hit-rgb-color"></a>Colore RGB raggiunto

Se si usano i pulsanti Region (PushHit, ToggleHit e 2PushHit), è necessario definire il colore che verrà usato da Windows Media Player per determinare l'area di hit del pulsante. Questo valore deve essere specificato utilizzando tre numeri interi positivi separati da virgole. Questi numeri interi rappresentano la quantità di rosso, verde e blu per un colore bitmap e variano da 0 a 255.

> [!Note]  
> I tipi di pulsanti sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive.

 

È possibile usare qualsiasi colore per i valori, ma assicurarsi che ogni pulsante dell'area definito abbia un colore univoco nel file di immagine dell'area e che il valore del colore definito qui come numero corrisponda al colore effettivo usato nell'immagine dell'area.

La tabella seguente illustra alcuni colori tipici che è possibile usare.



| Valore       | Descrizione |
|-------------|-------------|
| 0, 0, 0       | Nero       |
| 255.255.255 | White       |
| 255, 0, 0     | Red         |
| 0255, 0     | Green       |
| 0, 0255     | Blu        |



 

Se non si usano i pulsanti Region, è necessario immettere quanto segue:


```C++
0,0,0

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




