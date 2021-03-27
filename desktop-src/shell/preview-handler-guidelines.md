---
description: Quando si fornisce un'anteprima, è necessario seguire le linee guida riportate di seguito.
title: Linee guida per il gestore di anteprime
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3538cc5d-afb6-4d43-b527-6c6e1d773b41
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e725d561056e78a88bd9eeabd00d90abda1f0343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882797"
---
# <a name="preview-handler-guidelines"></a><span data-ttu-id="45467-103">Linee guida per il gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="45467-103">Preview Handler Guidelines</span></span>

<span data-ttu-id="45467-104">Quando si fornisce un'anteprima, è necessario seguire le linee guida riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="45467-104">When you provide a preview, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="45467-105">Un'anteprima dovrebbe contenere un'interfaccia utente minima: è semplicemente un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="45467-105">A preview should contain minimal UI—it is simply a preview.</span></span> <span data-ttu-id="45467-106">Dovrebbe visualizzare solo il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="45467-106">It should display only the file content.</span></span> <span data-ttu-id="45467-107">Non devono essere visualizzate finestre di dialogo, schermate iniziali, barre degli strumenti o riquadri attività.</span><span class="sxs-lookup"><span data-stu-id="45467-107">It should not display dialogs, splash screens, toolbars, or task panes.</span></span> <span data-ttu-id="45467-108">Il riquadro di lettura verrà usato in genere insieme alla ricerca per identificare rapidamente un file.</span><span class="sxs-lookup"><span data-stu-id="45467-108">The reading pane will commonly be used in conjunction with search to quickly identify a file.</span></span> <span data-ttu-id="45467-109">È consigliabile evitare qualsiasi elemento che ingombra il riquadro di lettura o altrimenti si sottrae dal contenuto del file o causa un ritardo nella visualizzazione dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="45467-109">Anything that clutters the reading pane or otherwise detracts from file content or causes delays in preview display should be avoided.</span></span>
-   <span data-ttu-id="45467-110">L'anteprima dovrebbe consentire all'utente di spostarsi nel documento.</span><span class="sxs-lookup"><span data-stu-id="45467-110">The preview should allow the user to navigate in the document.</span></span> <span data-ttu-id="45467-111">L'utente deve inoltre essere in grado di selezionare e copiare il testo.</span><span class="sxs-lookup"><span data-stu-id="45467-111">The user should also be able to select and copy text.</span></span>
-   <span data-ttu-id="45467-112">L'anteprima non deve essere a elevato utilizzo di memoria, deve utilizzare risorse minime e deve avere un tempo di avvio rapido.</span><span class="sxs-lookup"><span data-stu-id="45467-112">The preview should not be memory-intensive, should consume minimal resources, and should have a fast startup time.</span></span>
-   <span data-ttu-id="45467-113">L'esecuzione di tutti gli script e le macro nel file visualizzato in anteprima dovrebbe essere bloccata a scopo di sicurezza e privacy.</span><span class="sxs-lookup"><span data-stu-id="45467-113">All script and macros in the file being previewed should be blocked from running for security and privacy purposes.</span></span>
-   <span data-ttu-id="45467-114">L'anteprima deve supportare tasti di scelta rapida per la navigazione e la selezione come supportato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="45467-114">The preview should support keyboard accelerators for navigation and selection as supported by the application.</span></span> <span data-ttu-id="45467-115">Deve inoltre visualizzare un menu di scelta rapida quando si fa clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="45467-115">It should also display a context menu when right-clicked.</span></span>
-   <span data-ttu-id="45467-116">Quando un file viene visualizzato come anteprima, l'anteprima non deve bloccare il file stesso.</span><span class="sxs-lookup"><span data-stu-id="45467-116">When a file is displayed as a preview, the preview should not lock the file itself.</span></span> <span data-ttu-id="45467-117">Un file può essere visualizzato in anteprima e aperto nell'applicazione associata nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="45467-117">A file can be previewed and opened in its associated application at the same time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45467-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45467-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45467-119">Gestori di anteprime e host di anteprima della shell</span><span class="sxs-lookup"><span data-stu-id="45467-119">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="45467-120">Compilazione di gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="45467-120">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> </dl>

 

 



