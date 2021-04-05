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
# <a name="using-javascript-and-jscript"></a><span data-ttu-id="c8445-103">Utilizzo di JavaScript e JScript</span><span class="sxs-lookup"><span data-stu-id="c8445-103">Using JavaScript and JScript</span></span>

<span data-ttu-id="c8445-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8445-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c8445-105">Se si utilizza JavaScript o Microsoft JScript per accedere all'interfaccia di programmazione dell'agente Microsoft, attenersi alle convenzioni per questa lingua per specificare metodi o proprietà:</span><span class="sxs-lookup"><span data-stu-id="c8445-105">If you use JavaScript or Microsoft JScript to access Microsoft Agent's programming interface, follow the conventions for this language for specifying methods or properties:</span></span>

``` syntax
agent.object.Method (parameter)
agent.object.Property = value
```

<span data-ttu-id="c8445-106">JavaScript attualmente non dispone di una sintassi di evento per oggetti non HTML.</span><span class="sxs-lookup"><span data-stu-id="c8445-106">JavaScript does not currently have event syntax for non-HTML objects.</span></span> <span data-ttu-id="c8445-107">Tuttavia, con Internet Explorer è possibile usare il `<SCRIPT>` tag **per...** Sintassi dell'evento:</span><span class="sxs-lookup"><span data-stu-id="c8445-107">However, with Internet Explorer you can use the `<SCRIPT>` tag's **For...Event** syntax:</span></span>

``` syntax
<SCRIPT LANGUAGE="JScript" FOR="object" EVENT="event()">
statements
</SCRIPT>
```

<span data-ttu-id="c8445-108">Poiché non tutti i browser supportano attualmente questa sintassi di evento, è consigliabile utilizzare JavaScript solo per le pagine che supportano Microsoft Internet Explorer o per il codice che non richiede la gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="c8445-108">Because not all browsers currently support this event syntax, you may want to use JavaScript only for pages that support Microsoft Internet Explorer or for code that does not require event handling.</span></span>

<span data-ttu-id="c8445-109">Per accedere alle raccolte di oggetti dell'agente, utilizzare la funzione di [**enumeratore**](https://www.bing.com/search?q=**Enumerator**) JScript.</span><span class="sxs-lookup"><span data-stu-id="c8445-109">To access Agent's object collections, use the JScript [**Enumerator**](https://www.bing.com/search?q=**Enumerator**) function.</span></span> <span data-ttu-id="c8445-110">Tuttavia, le versioni di JScript incluse prima di Internet Explorer 4,0 non supportano questa funzione e non supportano le raccolte.</span><span class="sxs-lookup"><span data-stu-id="c8445-110">However, versions of JScript included prior to Internet Explorer 4.0 do not support this function and do not support collections.</span></span> <span data-ttu-id="c8445-111">Per accedere ai metodi e alle proprietà dell'oggetto [**character**](/windows/desktop/lwef/the-characters-object) , utilizzare il metodo [**character**](character-method.md) .</span><span class="sxs-lookup"><span data-stu-id="c8445-111">To access methods and properties of the [**Character**](/windows/desktop/lwef/the-characters-object) object, use the [**Character**](character-method.md) method.</span></span> <span data-ttu-id="c8445-112">Analogamente, per accedere alle proprietà di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) , utilizzare il metodo [**Command**](command-method.md) .</span><span class="sxs-lookup"><span data-stu-id="c8445-112">Similarly, to access the properties of a [**Command**](/windows/desktop/lwef/the-command-object) object, use the [**Command**](command-method.md) method.</span></span>

 

 