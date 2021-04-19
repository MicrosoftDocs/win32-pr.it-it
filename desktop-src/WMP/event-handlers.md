---
title: Gestori di eventi
description: Gestori di eventi
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Windows Media Player Skin, gestori eventi in JScript
- interfacce, gestori eventi in JScript
- eventi, JScript
- File JScript per interfacce, gestori eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297627"
---
# <a name="event-handlers"></a><span data-ttu-id="48902-107">Gestori di eventi</span><span class="sxs-lookup"><span data-stu-id="48902-107">Event Handlers</span></span>

<span data-ttu-id="48902-108">Microsoft JScript viene utilizzato per elaborare gli eventi nel file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="48902-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="48902-109">Per ulteriori informazioni sui gestori eventi, vedere [gestione degli eventi](handling-events.md) .</span><span class="sxs-lookup"><span data-stu-id="48902-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="48902-110">È possibile avere più di una riga di codice in un gestore eventi, ma è necessario prestare attenzione a non superare la lunghezza di riga consentita da JScript.</span><span class="sxs-lookup"><span data-stu-id="48902-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="48902-111">Separare le righe con un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="48902-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="48902-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48902-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48902-113">**Utilizzo di JScript**</span><span class="sxs-lookup"><span data-stu-id="48902-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




