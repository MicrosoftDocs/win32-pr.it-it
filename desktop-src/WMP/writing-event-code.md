---
title: Scrittura del codice evento
description: Scrittura del codice evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player Skin, scrittura di codice
- interfacce, scrittura di codice
- eventi, scrittura di codice
- scrittura di codice per interfacce, informazioni
- Windows Media Player Skin, eventi
- interfacce, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045321"
---
# <a name="writing-event-code"></a><span data-ttu-id="4d4ca-109">Scrittura del codice evento</span><span class="sxs-lookup"><span data-stu-id="4d4ca-109">Writing Event Code</span></span>

<span data-ttu-id="4d4ca-110">Gli eventi vengono trattati in modo analogo agli attributi.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="4d4ca-111">È necessario assegnare un valore all'evento e il valore è il codice che si desidera eseguire quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="4d4ca-112">La parola "on" viene aggiunta all'inizio del nome dell'evento; ad esempio, l'evento Click diventerà **OnClick**.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="4d4ca-113">Il valore dell'evento è racchiuso tra virgolette doppie e inizia con la parola JScript seguita da due punti.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="4d4ca-114">Il codice che si vuole eseguire è successivo, seguito da un punto e virgola e dalle virgolette doppie di chiusura.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="4d4ca-115">Ad esempio, per arrestare la riproduzione quando l'utente fa clic su un pulsante, digitare quanto segue come attributo nel codice dell'elemento **Button** :</span><span class="sxs-lookup"><span data-stu-id="4d4ca-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="4d4ca-116">Se si dispone di un codice che richiede virgolette, usare le virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="4d4ca-117">È necessario prestare attenzione quando si usano le virgolette in modo che siano bilanciate correttamente.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="4d4ca-118">Di seguito è riportato un esempio di utilizzo di entrambi i tipi:</span><span class="sxs-lookup"><span data-stu-id="4d4ca-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="4d4ca-119">È anche possibile modificare gli attributi dell'interfaccia quando si gestisce un evento esterno.</span><span class="sxs-lookup"><span data-stu-id="4d4ca-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="4d4ca-120">Per chiudere, ad esempio, una vista denominata visualizzazione, è possibile digitare:</span><span class="sxs-lookup"><span data-stu-id="4d4ca-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="4d4ca-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d4ca-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d4ca-122">**Gestione degli eventi**</span><span class="sxs-lookup"><span data-stu-id="4d4ca-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




