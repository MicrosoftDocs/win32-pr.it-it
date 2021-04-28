---
description: Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116359"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="7ae6e-103">Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità</span><span class="sxs-lookup"><span data-stu-id="7ae6e-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="7ae6e-104">Questa sezione descrive i passaggi di mitigazione di base e come pianificare la compatibilità futura delle applicazioni mentre si stanno affrontando i problemi.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="7ae6e-105">Windows Internet Explorer supporta i modelli Internet Explorer legacy ogni volta che è possibile, in modo che i siti che si sviluppano continuino a comportarsi come previsto nelle versioni più recenti di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="7ae6e-106">A partire da Windows Internet Explorer 8, è possibile scegliere di supportare i comportamenti legacy selezionando la modalità di rendering pagina per pagina.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="7ae6e-107">Internet Explorer 8 include le modalità di rendering seguenti che è possibile impostare usando l'intestazione compatibile con X-UA.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="7ae6e-108">Valore di content</span><span class="sxs-lookup"><span data-stu-id="7ae6e-108">Content value</span></span> | <span data-ttu-id="7ae6e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ae6e-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae6e-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="7ae6e-110">IE=5</span></span>          | <span data-ttu-id="7ae6e-111">Usare la modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="7ae6e-112">IE=7</span><span class="sxs-lookup"><span data-stu-id="7ae6e-112">IE=7</span></span>          | <span data-ttu-id="7ae6e-113">Usare sempre la modalità windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="7ae6e-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="7ae6e-114">IE=EmulateIE7</span></span> | <span data-ttu-id="7ae6e-115">Visualizzare in Internet Explorer 7, a meno che il sito non abbia i caratteri DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="7ae6e-116">IE=8</span><span class="sxs-lookup"><span data-stu-id="7ae6e-116">IE=8</span></span>          | <span data-ttu-id="7ae6e-117">Usare sempre Internet Explorer modalità 8.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="7ae6e-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="7ae6e-118">IE=EmulateIE8</span></span> | <span data-ttu-id="7ae6e-119">Eseguire Visualizzazione Compatibilità nei computer client e usare Internet Explorer modalità 8.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="7ae6e-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="7ae6e-120">IE=Edge</span></span>       | <span data-ttu-id="7ae6e-121">Visualizzare nella modalità più recente.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-121">Display in the latest mode.</span></span> <span data-ttu-id="7ae6e-122">In Internet Explorer 8, questo valore equivale a IE=8.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="7ae6e-123">Negli argomenti seguenti viene descritto come aggiornare le applicazioni Web usando Visualizzazione Compatibilità.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="7ae6e-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="7ae6e-124">Topic</span></span>                                                                                                  | <span data-ttu-id="7ae6e-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ae6e-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae6e-126">Informazioni Visualizzazione Compatibilità</span><span class="sxs-lookup"><span data-stu-id="7ae6e-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="7ae6e-127">Descrive Visualizzazione Compatibilità.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="7ae6e-128">Perché è necessario Visualizzazione Compatibilità?</span><span class="sxs-lookup"><span data-stu-id="7ae6e-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="7ae6e-129">Descrive il motivo per cui è consigliabile usare Visualizzazione Compatibilità.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="7ae6e-130">Usare il meta tag per garantire la compatibilità futura</span><span class="sxs-lookup"><span data-stu-id="7ae6e-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="7ae6e-131">Viene descritto come usare l'elemento **meta** per garantire la compatibilità futura.</span><span class="sxs-lookup"><span data-stu-id="7ae6e-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



