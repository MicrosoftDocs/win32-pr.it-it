---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript Object Notation (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232030"
---
# <a name="javascript-object-notation-json"></a><span data-ttu-id="b83ec-103">JavaScript Object Notation (JSON)</span><span class="sxs-lookup"><span data-stu-id="b83ec-103">JavaScript Object Notation (JSON)</span></span>

<span data-ttu-id="b83ec-104">[JavaScript Object Notation (JSON)](https://www.json.org/) è un formato di interscambio dati semplice e leggero basato su un subset della notazione del valore letterale dell'oggetto del linguaggio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b83ec-104">[JavaScript Object Notation (JSON)](https://www.json.org/) is a simple and lightweight data-interchange format that is based on a subset of the object literal notation of the JavaScript language.</span></span> <span data-ttu-id="b83ec-105">Il motore JavaScript in Windows Internet Explorer 8 implementa la [proposta json 3,1 JSON](https://www.ecma-international.org/) per le funzioni native di gestione JSON, che usa l' [API json2.js di Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span><span class="sxs-lookup"><span data-stu-id="b83ec-105">The JavaScript engine in Windows Internet Explorer 8 implements the [ECMAScript 3.1 JSON proposal](https://www.ecma-international.org/) for native JSON-handling functions (which uses [Douglas Crockford's json2.js API](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)).</span></span>

<span data-ttu-id="b83ec-106">Internet Explorer 8 include un oggetto JSON nativo che è conforme al supporto JSON descritto nella [bozza di lavoro della proposta es 3.1](https://www.ecma-international.org/).</span><span class="sxs-lookup"><span data-stu-id="b83ec-106">Internet Explorer 8 includes a native JSON object that complies with the JSON support that is described in the [ES3.1 Proposal Working Draft](https://www.ecma-international.org/).</span></span> <span data-ttu-id="b83ec-107">Alcune pagine web rilevano l'oggetto JSON nativo e quindi lo usano in modo non standard.</span><span class="sxs-lookup"><span data-stu-id="b83ec-107">Some webpages detect the native JSON object, and then use it in a non-standard way.</span></span> <span data-ttu-id="b83ec-108">Questo utilizzo causa in genere un errore di script e interrompe la gestione delle richieste AJAX.</span><span class="sxs-lookup"><span data-stu-id="b83ec-108">This usage typically causes a script error and breaks the handling of AJAX requests.</span></span> <span data-ttu-id="b83ec-109">Nell'esempio di codice seguente viene illustrato il modo errato di utilizzare l'oggetto JSON.</span><span class="sxs-lookup"><span data-stu-id="b83ec-109">The following code example shows the wrong way to use the JSON object.</span></span>


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



<span data-ttu-id="b83ec-110">Al contrario, l'esempio di codice seguente illustra un modo efficace per usare l'oggetto JSON.</span><span class="sxs-lookup"><span data-stu-id="b83ec-110">Instead, the following code example shows a good way to use the JSON object.</span></span>


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



<span data-ttu-id="b83ec-111">Windows Internet Explorer include i supporti nativi per JSON introducendo un oggetto JSON globale con due metodi predefiniti: **stringify** e **Parse**.</span><span class="sxs-lookup"><span data-stu-id="b83ec-111">Windows Internet Explorer includes native supports for JSON by introducing a global JSON object that has two built-in methods: **stringify** and **parse**.</span></span> <span data-ttu-id="b83ec-112">L'oggetto JSON globale è definito nel motore JavaScript e viene creato durante la fase di inizializzazione del motore.</span><span class="sxs-lookup"><span data-stu-id="b83ec-112">The global JSON object is defined in the JavaScript engine and is created during the engine initialization phase.</span></span> <span data-ttu-id="b83ec-113">Per mantenere la compatibilità con le versioni precedenti, questa funzionalità è disponibile solo quando un sito Web usa la versione più recente delle funzionalità JavaScript usando la modalità di layout (documento) "standard di Internet Explorer 8".</span><span class="sxs-lookup"><span data-stu-id="b83ec-113">To maintain backward compatibility, this feature is available only when a website uses the latest version of JavaScript features by using the "Internet Explorer 8 Standards" layout (document) mode.</span></span> <span data-ttu-id="b83ec-114">Questa funzionalità può anche influire sul comportamento delle pagine Web che dipendono da una variabile globale JSON o usano [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span><span class="sxs-lookup"><span data-stu-id="b83ec-114">This feature also might affect the behavior of webpages that depend on a global variable JSON or use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).</span></span>

<span data-ttu-id="b83ec-115">È possibile eseguire l'override dell'oggetto JSON globale.</span><span class="sxs-lookup"><span data-stu-id="b83ec-115">You can override the global JSON object.</span></span> <span data-ttu-id="b83ec-116">Tuttavia, quando una pagina Web utilizza la modalità layout (documento) "standard di Internet Explorer 8", non è più un oggetto non definito.</span><span class="sxs-lookup"><span data-stu-id="b83ec-116">But when a webpage uses the “Internet Explorer 8 Standards” layout (document) mode, it is not an undefined object anymore.</span></span> <span data-ttu-id="b83ec-117">Poiché viene creata un'istanza di JSON come nome globale dal motore JavaScript, i controlli come "if (! this.JSON)" restituiscono false e devono essere modificati nel codice utente.</span><span class="sxs-lookup"><span data-stu-id="b83ec-117">Because JSON is instantiated as a global name by the JavaScript engine, checks like "if(!this.JSON)" evaluate to False and must be changed in the user code.</span></span>

<span data-ttu-id="b83ec-118">È probabile che le pagine Web che usano [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) non siano interessate.</span><span class="sxs-lookup"><span data-stu-id="b83ec-118">Webpages that use [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) are likely not affected.</span></span> <span data-ttu-id="b83ec-119">Con poche eccezioni, queste pagine dovrebbero funzionare più velocemente.</span><span class="sxs-lookup"><span data-stu-id="b83ec-119">With few exceptions, these pages should work faster.</span></span> <span data-ttu-id="b83ec-120">Le eccezioni sono dovute alle differenze tra l'implementazione JSON nativa di Internet Explorer e la json2.js.</span><span class="sxs-lookup"><span data-stu-id="b83ec-120">The exceptions are because of the differences between the Internet Explorer native JSON implementation and json2.js.</span></span> <span data-ttu-id="b83ec-121">Ad esempio, durante la serializzazione, l'implementazione JSON nativa rileva i cicli e non entra in una ricorsione infinita come json.js.</span><span class="sxs-lookup"><span data-stu-id="b83ec-121">For example, during serialization, the native JSON implementation detects cycles and does not go in infinite recursion like json.js.</span></span> <span data-ttu-id="b83ec-122">Per ulteriori informazioni su queste eccezioni, vedere i [Blog di JavaScript](/archive/blogs/jscript/).</span><span class="sxs-lookup"><span data-stu-id="b83ec-122">For more information about these exceptions, see the [JavaScript Blogs](/archive/blogs/jscript/).</span></span>

<span data-ttu-id="b83ec-123">Per ulteriori informazioni, vedere la [documentazione JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) e [il controllo delle versioni e il supporto della versione del motore JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span><span class="sxs-lookup"><span data-stu-id="b83ec-123">For more information, see [JSON Documentation](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) and [Versioning and JavaScript Engine’s Version Support](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b83ec-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b83ec-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b83ec-125">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="b83ec-125">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
