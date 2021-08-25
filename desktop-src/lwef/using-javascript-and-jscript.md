---
title: Uso di JavaScript e JScript
description: Uso di JavaScript e JScript
ms.assetid: c6927663-9432-4fa9-8de6-abb7237909b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3b32fd3d8e2c8ce9e337f489c27dadaa32bb379d6bc90c6083d62af52bee24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960681"
---
# <a name="using-javascript-and-jscript"></a>Uso di JavaScript e JScript

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Se si usa JavaScript o Microsoft JScript per accedere all'interfaccia di programmazione di Microsoft Agent, seguire le convenzioni per questo linguaggio per specificare metodi o proprietà:

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

JavaScript non dispone attualmente della sintassi degli eventi per gli oggetti non HTML. Tuttavia, con Internet Explorer è possibile usare il `<SCRIPT>` tag **For... Sintassi dell'evento:**

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

Poiché non tutti i browser supportano attualmente questa sintassi degli eventi, è possibile usare JavaScript solo per le pagine che supportano Microsoft Internet Explorer o per il codice che non richiede la gestione degli eventi.

Per accedere alle raccolte di oggetti di Agent, usare la JScript [**Enumeratore.**](https://www.bing.com/search?q=**Enumerator**) Tuttavia, le versioni JScript precedenti Internet Explorer 4.0 non supportano questa funzione e non supportano le raccolte. Per accedere ai metodi e alle proprietà [**dell'oggetto Character,**](/windows/desktop/lwef/the-characters-object) usare il [**metodo Character.**](character-method.md) Analogamente, per accedere alle proprietà di un [**oggetto Command,**](/windows/desktop/lwef/the-command-object) usare il [**metodo Command.**](command-method.md)

 

 