---
title: Eventi esterni
description: Eventi esterni
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player, eventi esterni
- interfaccia, eventi esterni
- eventi, esterni
- scrittura di codice per le interfaccia, eventi esterni
- eventi esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91232447e37bc3970ea8dd0ec727fb9b5daae65e647809b129df3e0347c496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649191"
---
# <a name="external-events"></a>Eventi esterni

Quando gli utenti selezionano un pulsante o premono un tasto, è possibile rispondere all'input con i gestori eventi. Un gestore eventi è una sezione di codice che viene eseguita ogni volta che viene attivato l'evento.

Gli eventi seguenti sono supportati dagli elementi dell'interfaccia:

-   **carico**
-   **close**
-   **Ridimensionare**
-   **Timer**
-   **Fare clic su**
-   **Dblclick**
-   **error**
-   **Mousedown**
-   **Mouseup**
-   **Mousemove**
-   **Mouseover**
-   **mouseout**
-   **Keypress**
-   **Keydown**
-   **Keyup**

Per altri [dettagli su eventi](skin-programming-reference.md) specifici, vedere Guida di riferimento alla programmazione dell'interfaccia.

Un tipico gestore eventi esterno denota l'evento e definisce il codice che verrà eseguito. Ad esempio, se si vuole creare codice per iniziare Windows Media Player quando l'utente fa clic su un pulsante, inserire la riga seguente nel codice del pulsante.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Verrà riprodotto il file denominato laure.wma. Si noti che si aggiunge la parola "on" a eventi specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




