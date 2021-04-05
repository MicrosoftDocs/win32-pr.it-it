---
title: Utilizzo di JavaScript e JScript
description: Utilizzo di JavaScript e JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fbac6d69de69daecbf21c50aafdafce81ed9d95
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117699"
---
# <a name="using-javascript-and-jscript"></a>Utilizzo di JavaScript e JScript

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Se si utilizza JavaScript o Microsoft JScript per accedere all'interfaccia di programmazione dell'agente Microsoft, attenersi alle convenzioni per questa lingua per specificare metodi o proprietà:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript attualmente non dispone di una sintassi di evento per oggetti non HTML. Tuttavia, con Internet Explorer è possibile usare il `<SCRIPT>` tag **per...** Sintassi dell'evento:

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Poiché non tutti i browser supportano attualmente questa sintassi di evento, è consigliabile utilizzare JavaScript solo per le pagine che supportano Microsoft Internet Explorer o per il codice che non richiede la gestione degli eventi.

Per accedere alle raccolte di oggetti dell'agente, utilizzare la funzione di [**enumeratore**](https://www.bing.com/search?q=**Enumerator**) JScript. Tuttavia, le versioni di JScript incluse prima di Internet Explorer 4,0 non supportano questa funzione e non supportano le raccolte. Per accedere ai metodi e alle proprietà dell'oggetto [**character**](/windows/desktop/lwef/the-characters-object) , utilizzare il metodo [**character**](character-method.md) . Analogamente, per accedere alle proprietà di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) , utilizzare il metodo [**Command**](command-method.md) .

 

 