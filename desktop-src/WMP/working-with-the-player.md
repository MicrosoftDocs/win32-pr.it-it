---
title: Utilizzo del lettore
description: Utilizzo del lettore
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player Skin, attributo Player in JScript
- interfacce, attributo Player in JScript
- attributi, lettore
- attributo Player
- File JScript per interfacce, attributo Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396879"
---
# <a name="working-with-the-player"></a>Utilizzo del lettore

Quando si utilizza Microsoft JScript per accedere ai metodi e alle proprietà di Media Player di Windows, è necessario utilizzare il nome "Player" per il nome del controllo. Per fare riferimento al metodo Stop, ad esempio, è necessario digitare quanto segue:


```C++
player.Controls.Stop()

```



L'attributo globale **Player** è la chiave per accedere al controllo Media Player Windows tramite lo script dell'interfaccia. Tramite questo attributo, tutti gli oggetti del controllo Media Player di Windows diventano accessibili per la modifica in fase di esecuzione tramite le proprietà e i metodi. Inoltre, l'elemento **Player** è disponibile, in modo che sia possibile specificare i gestori eventi e l'attributo **URL** in fase di progettazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo di JScript**](using-jscript.md)
</dt> </dl>

 

 




