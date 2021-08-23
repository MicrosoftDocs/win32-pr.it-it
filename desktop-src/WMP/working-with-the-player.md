---
title: Uso del lettore
description: Uso del lettore
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player, attributo player in JScript
- skins,player attribute in JScript
- attributi, lettore
- Attributo player
- JScript per le interfaccia, attributo player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77098f161244488d5097d2d022f105628a43ba50a40218da01295d99f2de0cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566983"
---
# <a name="working-with-the-player"></a>Uso del lettore

Quando si usa Microsoft JScript per accedere ai metodi e alle proprietà di Windows Media Player, è necessario usare il nome "player" come nome del controllo. Ad esempio, per fare riferimento al metodo Stop, è necessario digitare:


```C++
player.Controls.Stop()

```



**L'attributo globale** del lettore è la chiave per accedere al controllo Windows Media Player tramite script dell'interfaccia. Tramite questo attributo, tutti gli oggetti del controllo Windows Media Player diventano accessibili per la modifica in fase di esecuzione tramite le relative proprietà e metodi. Inoltre, **l'elemento PLAYER** è disponibile in modo che sia possibile specificare i gestori eventi e l'attributo **url** in fase di progettazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di JScript**](using-jscript.md)
</dt> </dl>

 

 




