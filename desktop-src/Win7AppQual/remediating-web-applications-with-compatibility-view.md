---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320641"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a><span data-ttu-id="4b308-103">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="4b308-103">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>

<span data-ttu-id="4b308-104">In questa sezione vengono descritti i passaggi di mitigazione di base e viene illustrato come pianificare la compatibilità delle applicazioni in futuro mentre si sta risolvendo immediatamente eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="4b308-104">This section describes basic mitigation steps and how to plan for future application compatibility while you are addressing any issues now.</span></span>

<span data-ttu-id="4b308-105">Windows Internet Explorer supporta i modelli di Internet Explorer legacy ogni volta che è possibile, in modo che i siti sviluppati continuino a comportarsi come previsto nelle versioni più recenti di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4b308-105">Windows Internet Explorer supports the legacy Internet Explorer models whenever feasible so that sites that you develop to them continue to behave as expected in newer versions of Internet Explorer.</span></span> <span data-ttu-id="4b308-106">A partire da Windows Internet Explorer 8, è possibile scegliere di supportare i comportamenti legacy selezionando la modalità di rendering in base alla pagina.</span><span class="sxs-lookup"><span data-stu-id="4b308-106">Starting with Windows Internet Explorer 8, you can choose to support legacy behaviors by selecting the rendering mode on a page-by-page basis.</span></span>

<span data-ttu-id="4b308-107">Internet Explorer 8 include le modalità di rendering seguenti che è possibile impostare utilizzando l'intestazione X-UA-Compatible.</span><span class="sxs-lookup"><span data-stu-id="4b308-107">Internet Explorer 8 includes the following rendering modes that you can set by using the X-UA-Compatible header.</span></span>



| <span data-ttu-id="4b308-108">Valore di content</span><span class="sxs-lookup"><span data-stu-id="4b308-108">Content value</span></span> | <span data-ttu-id="4b308-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b308-109">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b308-110">IE=5</span><span class="sxs-lookup"><span data-stu-id="4b308-110">IE=5</span></span>          | <span data-ttu-id="4b308-111">Utilizzare la modalità non standard.</span><span class="sxs-lookup"><span data-stu-id="4b308-111">Use quirks mode.</span></span>                                                                      |
| <span data-ttu-id="4b308-112">IE = 7</span><span class="sxs-lookup"><span data-stu-id="4b308-112">IE=7</span></span>          | <span data-ttu-id="4b308-113">Utilizzare sempre la modalità Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="4b308-113">Always use Windows Internet Explorer 7 mode.</span></span>                                          |
| <span data-ttu-id="4b308-114">IE=EmulateIE7</span><span class="sxs-lookup"><span data-stu-id="4b308-114">IE=EmulateIE7</span></span> | <span data-ttu-id="4b308-115">Viene visualizzato in modalità Internet Explorer 7, a meno che il sito non disponga di un DOCTYPE non standard.</span><span class="sxs-lookup"><span data-stu-id="4b308-115">Display in Internet Explorer 7 mode unless the site has the quirks DOCTYPE.</span></span>           |
| <span data-ttu-id="4b308-116">IE = 8</span><span class="sxs-lookup"><span data-stu-id="4b308-116">IE=8</span></span>          | <span data-ttu-id="4b308-117">Utilizzare sempre la modalità Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="4b308-117">Always use Internet Explorer 8 mode.</span></span>                                                  |
| <span data-ttu-id="4b308-118">IE=EmulateIE8</span><span class="sxs-lookup"><span data-stu-id="4b308-118">IE=EmulateIE8</span></span> | <span data-ttu-id="4b308-119">Eseguire l'override della visualizzazione compatibilità nei computer client e utilizzare la modalità Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="4b308-119">Override Compatibility View on client machines and use Internet Explorer 8 mode.</span></span>      |
| <span data-ttu-id="4b308-120">IE=Edge</span><span class="sxs-lookup"><span data-stu-id="4b308-120">IE=Edge</span></span>       | <span data-ttu-id="4b308-121">Viene visualizzato nella modalità più recente.</span><span class="sxs-lookup"><span data-stu-id="4b308-121">Display in the latest mode.</span></span> <span data-ttu-id="4b308-122">In Internet Explorer 8, questo valore è equivalente a IE = 8.</span><span class="sxs-lookup"><span data-stu-id="4b308-122">In Internet Explorer 8, this value is equivalent to IE=8.</span></span> |



 

<span data-ttu-id="4b308-123">Negli argomenti seguenti viene descritto come aggiornare le applicazioni Web utilizzando visualizzazione compatibilità.</span><span class="sxs-lookup"><span data-stu-id="4b308-123">The following topics describe how to update web applications by using Compatibility View.</span></span>



| <span data-ttu-id="4b308-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="4b308-124">Topic</span></span>                                                                                                  | <span data-ttu-id="4b308-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b308-125">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="4b308-126">Informazioni sulla visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="4b308-126">What Is Compatibility View</span></span>](what-is-compatibility-view-.md)                                          | <span data-ttu-id="4b308-127">Viene descritta la visualizzazione compatibilità.</span><span class="sxs-lookup"><span data-stu-id="4b308-127">Describes Compatibility View.</span></span>                                                  |
| [<span data-ttu-id="4b308-128">Perché è necessaria la visualizzazione compatibilità?</span><span class="sxs-lookup"><span data-stu-id="4b308-128">Why Do You Need Compatibility View?</span></span>](why-do-you-need-compatibility-view-.md)                         | <span data-ttu-id="4b308-129">Viene descritto il motivo per cui è consigliabile utilizzare la visualizzazione compatibilità.</span><span class="sxs-lookup"><span data-stu-id="4b308-129">Describes why you should use Compatibility View.</span></span>                               |
| [<span data-ttu-id="4b308-130">Usare il tag meta per garantire la compatibilità futura</span><span class="sxs-lookup"><span data-stu-id="4b308-130">Use the Meta Tag to Ensure Future Compatibility</span></span>](use-the-meta-tag-to-ensure-future-compatibility.md) | <span data-ttu-id="4b308-131">Viene descritto come utilizzare l'elemento **meta** per garantire la compatibilità futura.</span><span class="sxs-lookup"><span data-stu-id="4b308-131">Describes how you can use the **meta** element to ensure future compatibility.</span></span> |



 

 

 



