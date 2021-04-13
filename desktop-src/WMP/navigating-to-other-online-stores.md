---
title: Spostamento in altri archivi online
description: Spostamento in altri archivi online
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player Online Stores, spostamento
- negozi online, esplorazione
- digitare 2 archivi online, spostamento
- spostamento nei negozi online di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328292"
---
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="58e69-107">Spostamento in altri archivi online</span><span class="sxs-lookup"><span data-stu-id="58e69-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="58e69-108">È possibile creare collegamenti ad altri negozi online di cui si è proprietari o a un collegamento incrociato a negozi online forniti da altri utenti.</span><span class="sxs-lookup"><span data-stu-id="58e69-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="58e69-109">A tale scopo, è necessario individuare il nome della chiave per lo Store online in cui si desidera spostarsi.</span><span class="sxs-lookup"><span data-stu-id="58e69-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="58e69-110">Il codice di esempio seguente mostra il codice HTML che consente di creare un collegamento per passare da Proseware Online Store alla funzionalità "ServiceTask2" di Southridge Video Online Store:</span><span class="sxs-lookup"><span data-stu-id="58e69-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="58e69-111">Quando l'utente fa clic sul collegamento, Windows Media Player chiede all'utente di passare all'archivio video Southridge.</span><span class="sxs-lookup"><span data-stu-id="58e69-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="58e69-112">Se l'utente lo consente, il lettore passa a archivia e passa al riquadro attività specificato, aggiungendo i parametri della stringa di query.</span><span class="sxs-lookup"><span data-stu-id="58e69-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="58e69-113">I parametri della stringa di query illustrati nell'esempio precedente sono parametri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="58e69-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="58e69-114">Ciò significa che il negozio online a cui si passa deve aspettarsi questi valori e gestirli.</span><span class="sxs-lookup"><span data-stu-id="58e69-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="58e69-115">L'archivio online (e qualsiasi archivio a cui si passa) può usare i parametri della stringa di query nel modo scelto.</span><span class="sxs-lookup"><span data-stu-id="58e69-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58e69-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58e69-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e69-117">**Spostamento tra i riquadri attività del servizio**</span><span class="sxs-lookup"><span data-stu-id="58e69-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="58e69-118">**Navigazione per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="58e69-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




