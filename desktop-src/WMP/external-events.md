---
title: Eventi esterni
description: Eventi esterni
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player Skin, eventi esterni
- interfacce, eventi esterni
- eventi, esterni
- scrittura di codice per interfacce, eventi esterni
- eventi esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298799"
---
# <a name="external-events"></a>Eventi esterni

Quando gli utenti fanno clic su un pulsante o si preme un tasto, è possibile rispondere all'input con i gestori eventi. Un gestore eventi è una sezione di codice che viene eseguito ogni volta che viene attivato l'evento.

Gli eventi seguenti sono supportati dagli elementi Skin:

-   **carico**
-   **close**
-   **ridimensionare**
-   **timer**
-   **Clicca**
-   **DblClick**
-   **error**
-   **MouseDown**
-   **MouseUp**
-   **MouseMove**
-   **MouseOver**
-   **mouseout**
-   **KeyPress**
-   **KeyDown**
-   **KeyUp**

Per ulteriori informazioni su eventi specifici, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md) .

Un tipico gestore eventi esterno denominare l'evento e definire il codice che verrà eseguito. Se ad esempio si vuole creare codice per avviare Windows Media Player quando l'utente fa clic su un pulsante, inserire la riga seguente nel codice del pulsante.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Verrà riprodotto il file denominato Laure. WMA. Si noti che la parola "on" viene aggiunta a eventi specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




