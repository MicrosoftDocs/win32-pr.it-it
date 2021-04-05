---
title: Implementazione di CPluginWindow
description: Implementazione di CPluginWindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Plug-in di Windows Media Player, classe CPluginWindow
- plug-in, classe CPluginWindow
- plug-in dell'interfaccia utente, classe CPluginWindow
- Plug-in dell'interfaccia utente, classe CPluginWindow
- Classe CPluginWindow
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709073"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="370a2-109">Implementazione di CPluginWindow</span><span class="sxs-lookup"><span data-stu-id="370a2-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="370a2-110">La classe CPluginWindow fornisce l'interfaccia utente per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="370a2-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="370a2-111">Nel caso del plug-in di ricerca dell'interfaccia utente, questa classe contiene il codice per il pulsante **Cerca** e il codice che avvia la pagina di ricerca quando si fa clic sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="370a2-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="370a2-112">La procedura guidata fornisce un'implementazione di base di CPluginWindow nel file di intestazione CPluginWindow. h.</span><span class="sxs-lookup"><span data-stu-id="370a2-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="370a2-113">Per semplificare le operazioni, il plug-in di ricerca dell'interfaccia utente modificherà direttamente il file, anche se le aggiunte estese verrebbero normalmente inserite in un file CPluginWindow. cpp separato.</span><span class="sxs-lookup"><span data-stu-id="370a2-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="370a2-114">Nelle sezioni seguenti vengono descritte le operazioni necessarie per implementare CPluginWindow:</span><span class="sxs-lookup"><span data-stu-id="370a2-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="370a2-115">Mappa messaggi</span><span class="sxs-lookup"><span data-stu-id="370a2-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="370a2-116">Costruttore</span><span class="sxs-lookup"><span data-stu-id="370a2-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="370a2-117">Metodo OnPaint</span><span class="sxs-lookup"><span data-stu-id="370a2-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="370a2-118">Metodo OnCreate</span><span class="sxs-lookup"><span data-stu-id="370a2-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="370a2-119">Metodo OnSearch</span><span class="sxs-lookup"><span data-stu-id="370a2-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="370a2-120">Metodo LaunchPage</span><span class="sxs-lookup"><span data-stu-id="370a2-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="370a2-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="370a2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="370a2-122">**Guida alla programmazione di plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="370a2-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




