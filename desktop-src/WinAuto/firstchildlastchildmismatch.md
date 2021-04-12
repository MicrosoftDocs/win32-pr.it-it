---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396354"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="31e51-103">FirstChildLastChildMismatch</span><span class="sxs-lookup"><span data-stu-id="31e51-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="31e51-104">Testo</span><span class="sxs-lookup"><span data-stu-id="31e51-104">Text</span></span>

<span data-ttu-id="31e51-105">Quando si esegue la chiamata {0} dal nodo testato e quindi si chiama ripetutamente {1} , è terminata l'operazione figlio seguente: {2} .</span><span class="sxs-lookup"><span data-stu-id="31e51-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="31e51-106">Non corrisponde al risultato della chiamata al {3} nodo testato, che ha restituito: {4} .</span><span class="sxs-lookup"><span data-stu-id="31e51-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="31e51-107">Al contrario, l'elemento figlio deve segnalare come padre il nodo di test.</span><span class="sxs-lookup"><span data-stu-id="31e51-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="31e51-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="31e51-108">Type</span></span>

<span data-ttu-id="31e51-109">Errore</span><span class="sxs-lookup"><span data-stu-id="31e51-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="31e51-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31e51-110">Description</span></span>

<span data-ttu-id="31e51-111">Si è verificato un problema durante la navigazione tra gli elementi figlio dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="31e51-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="31e51-112">1.</span><span class="sxs-lookup"><span data-stu-id="31e51-112">1.</span></span> <span data-ttu-id="31e51-113">Implementazione di automazione interfaccia utente non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="31e51-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="31e51-114">Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="31e51-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="31e51-115">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="31e51-115">Possible causes</span></span>

<span data-ttu-id="31e51-116">Implementazione di automazione interfaccia utente non corretta o non valida.</span><span class="sxs-lookup"><span data-stu-id="31e51-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31e51-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31e51-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31e51-118">**IUIAutomationElement::GetCachedParent**</span><span class="sxs-lookup"><span data-stu-id="31e51-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="31e51-119">**IUIAutomationTreeWalker**</span><span class="sxs-lookup"><span data-stu-id="31e51-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




