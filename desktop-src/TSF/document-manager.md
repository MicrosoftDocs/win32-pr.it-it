---
title: Gestione documenti
description: Gestione documenti
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- Framework servizi di testo (TSF), gestione documenti
- TSF (Framework di servizi di testo), gestione documenti
- Servizi di testo, gestione documenti
- Applicazioni abilitate per TSF, gestione documenti
- gestione documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708914"
---
# <a name="document-manager"></a><span data-ttu-id="4dcbd-108">Gestione documenti</span><span class="sxs-lookup"><span data-stu-id="4dcbd-108">Document Manager</span></span>

## <a name="applications"></a><span data-ttu-id="4dcbd-109">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="4dcbd-109">Applications</span></span>

<span data-ttu-id="4dcbd-110">Per creare un oggetto di gestione documenti, un'applicazione chiama [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span><span class="sxs-lookup"><span data-stu-id="4dcbd-110">To create a document manager object an application calls [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr).</span></span> <span data-ttu-id="4dcbd-111">L'applicazione crea un oggetto di gestione documenti separato per ogni singolo documento gestito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-111">The application creates a separate document manager object for each individual document that the application maintains.</span></span> <span data-ttu-id="4dcbd-112">L'applicazione utilizza Gestione documenti per creare contesti di modifica, aggiungere un contesto allo stack del contesto e rimuovere un contesto dallo stack di contesto.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-112">The application uses the document manager to create edit contexts, add a context to the context stack and remove a context from the context stack.</span></span>

## <a name="text-services"></a><span data-ttu-id="4dcbd-113">Servizi di testo</span><span class="sxs-lookup"><span data-stu-id="4dcbd-113">Text Services</span></span>

<span data-ttu-id="4dcbd-114">Un servizio di testo non crea mai un oggetto di gestione documenti.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-114">A text service never creates a document manager object.</span></span> <span data-ttu-id="4dcbd-115">Al contrario, il servizio di testo ottiene l'oggetto gestione documenti attualmente attivo chiamando [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span><span class="sxs-lookup"><span data-stu-id="4dcbd-115">Instead, the text service obtains the currently active document manager object by calling [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus).</span></span> <span data-ttu-id="4dcbd-116">Un servizio di testo utilizza Gestione documenti per ottenere il contesto all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-116">A text service uses the document manager to obtain the context at the top of the stack.</span></span>

<span data-ttu-id="4dcbd-117">Un servizio di testo può inoltre utilizzare Gestione documenti per creare il proprio contesto e aggiungerlo e rimuoverlo dallo stack di contesto.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-117">A text service can also use the document manager to create its own context and add and remove it from the context stack.</span></span> <span data-ttu-id="4dcbd-118">Questa operazione viene in genere eseguita quando il servizio di testo deve visualizzare un'interfaccia utente modale, ad esempio quando viene visualizzato un elenco di parole per consentire all'utente di selezionare una parola.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-118">This is normally done when the text service must display some modal user interface, such as when a list of words is displayed to enable the user to select a word.</span></span> <span data-ttu-id="4dcbd-119">Quando viene visualizzato l'elenco, il servizio di testo inserisce il proprio contesto nello stack.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-119">When the list is displayed, the text service places its own context on the stack.</span></span> <span data-ttu-id="4dcbd-120">Quando l'elenco di parole viene eliminato, il servizio di testo rimuove il contesto dallo stack.</span><span class="sxs-lookup"><span data-stu-id="4dcbd-120">When the word list is dismissed, the text service removes its context from the stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dcbd-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4dcbd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dcbd-122">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="4dcbd-122">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="4dcbd-123">ITfThreadMgr:: CreateDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="4dcbd-123">ITfThreadMgr::CreateDocumentMgr</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[<span data-ttu-id="4dcbd-124">ITfThreadMgr:: GetFocus</span><span class="sxs-lookup"><span data-stu-id="4dcbd-124">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




