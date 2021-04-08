---
title: Raccolta AnimationNames
description: Raccolta AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856169"
---
# <a name="the-animationnames-collection"></a>Raccolta AnimationNames

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

La raccolta [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) è una raccolta speciale che contiene l'elenco dei nomi di animazione compilati per un carattere. È possibile utilizzare la raccolta per enumerare i nomi delle animazioni per un carattere. Ad esempio, in Visual Basic o VBScript (2,0 o versione successiva) è possibile accedere a questi nomi usando il **per ciascuno... Istruzioni successive** :


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Gli elementi della raccolta non hanno proprietà, quindi non è possibile accedere direttamente a singoli elementi.

Per. I caratteri ACF, la raccolta restituisce tutte le animazioni definite per il carattere, non solo quelle che sono state recuperate con il metodo [**Get**](get-method.md) .

 

 




