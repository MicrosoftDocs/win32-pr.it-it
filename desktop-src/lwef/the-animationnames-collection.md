---
title: Raccolta AnimationNames
description: Raccolta AnimationNames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c9ee781b836599ccf9689bfae974fd4cf3af32d75df2070e984ae9b6596f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960661"
---
# <a name="the-animationnames-collection"></a>Raccolta AnimationNames

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

La [**raccolta AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) è una raccolta speciale che contiene l'elenco dei nomi di animazione compilati per un carattere. È possibile usare la raccolta per enumerare i nomi delle animazioni per un carattere. Ad esempio, in Visual Basic o VBScript (2.0 o versione successiva) è possibile accedere a questi nomi usando **for each... Istruzioni** seguenti:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Gli elementi nella raccolta non hanno proprietà, pertanto non è possibile accedere direttamente ai singoli elementi.

Per. Caratteri ACF, la raccolta restituisce tutte le animazioni definite per il carattere, non solo quelle recuperate con il [**metodo Get.**](get-method.md)

 

 




