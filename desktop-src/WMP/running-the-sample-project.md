---
title: Esecuzione del progetto di esempio
description: Esecuzione del progetto di esempio
ms.assetid: d0c32a75-4d30-408b-8da8-3917f6fd6ea4
keywords:
- Windows Media Player Online Stores, esecuzione di progetti di esempio
- negozi online, esecuzione di progetti di esempio
- digitare 2 archivi online, esecuzione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- esecuzione di progetti di esempio
- esempi, digitare 2 archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8f42829add3ffbe5cc026f7dc2451513701fd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396379"
---
# <a name="running-the-sample-project"></a><span data-ttu-id="bd5af-111">Esecuzione del progetto di esempio</span><span class="sxs-lookup"><span data-stu-id="bd5af-111">Running the Sample Project</span></span>

<span data-ttu-id="bd5af-112">Il componente COM di esempio illustra la funzionalità fornita dai metodi di **IWMPSubscriptionServices** visualizzando una finestra di dialogo ogni volta che Windows Media Player chiama uno dei metodi.</span><span class="sxs-lookup"><span data-stu-id="bd5af-112">The sample COM component demonstrates the functionality provided by the methods of **IWMPSubscriptionServices** by displaying a dialog box whenever Windows Media Player calls one of the methods.</span></span> <span data-ttu-id="bd5af-113">Per verificarlo, è necessario innanzitutto aggiungere contenuto alla raccolta che contiene un attributo **contentdistributor** che corrisponde al servizio.</span><span class="sxs-lookup"><span data-stu-id="bd5af-113">To see this happen, you must first add some content to the library that contains a **ContentDistributor** attribute that matches your service.</span></span> <span data-ttu-id="bd5af-114">Vedere [aggiungere l'attributo contentdistributor](adding-the-contentdistributor-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="bd5af-114">See [Adding the ContentDistributor Attribute](adding-the-contentdistributor-attribute.md).</span></span> <span data-ttu-id="bd5af-115">Usare quindi Windows Media Player 10 o versione successiva per aprire lo Store online, riprodurre il contenuto premium e copiare il contenuto premium in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd5af-115">Then, use Windows Media Player 10 or later to open your online store, play your premium content, and copy your premium content to a device.</span></span> <span data-ttu-id="bd5af-116">Windows Media Player creerà un'istanza del componente COM di esempio e chiamerà i metodi quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="bd5af-116">Windows Media Player will instantiate the sample COM component and call methods when appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd5af-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd5af-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd5af-118">**Creazione del plug-in per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="bd5af-118">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




