---
title: Messaggi comunicati tramite interfacce utente
description: In questo argomento sono elencati i messaggi che un servizio directory può inviare da un'interfaccia utente.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Messaggi comunicati tramite interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044108"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="9a39b-104">Messaggi comunicati tramite interfacce utente</span><span class="sxs-lookup"><span data-stu-id="9a39b-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="9a39b-105">In questo argomento sono elencati i messaggi che un servizio directory può inviare da un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9a39b-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="9a39b-106">Messaggi della pagina di query comuni</span><span class="sxs-lookup"><span data-stu-id="9a39b-106">Common Query Page Messages</span></span>

<span data-ttu-id="9a39b-107">I messaggi seguenti vengono inviati a una pagina di estensione del modulo di query del servizio directory nella funzione di callback [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :</span><span class="sxs-lookup"><span data-stu-id="9a39b-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="9a39b-108">**\_CLEARFORM CQPM**</span><span class="sxs-lookup"><span data-stu-id="9a39b-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="9a39b-109">**\_Abilitazione di CQPM**</span><span class="sxs-lookup"><span data-stu-id="9a39b-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="9a39b-110">**CQPM \_ GETparameters**</span><span class="sxs-lookup"><span data-stu-id="9a39b-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="9a39b-111">**\_HANDLERSPECIFIC CQPM**</span><span class="sxs-lookup"><span data-stu-id="9a39b-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="9a39b-112">**Guida di CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="9a39b-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="9a39b-113">**\_inizializzazione CQPM**</span><span class="sxs-lookup"><span data-stu-id="9a39b-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="9a39b-114">**CQPM \_ permanente**</span><span class="sxs-lookup"><span data-stu-id="9a39b-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="9a39b-115">**versione di CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="9a39b-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="9a39b-116">**\_SETDEFAULTPARAMETERS CQPM**</span><span class="sxs-lookup"><span data-stu-id="9a39b-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="9a39b-117">Messaggi esterni</span><span class="sxs-lookup"><span data-stu-id="9a39b-117">Miscellaneous Messages</span></span>

<span data-ttu-id="9a39b-118">Nella tabella seguente sono elencati i messaggi che possono essere inviati da un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="9a39b-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="9a39b-119">Message</span><span class="sxs-lookup"><span data-stu-id="9a39b-119">Message</span></span>                  | <span data-ttu-id="9a39b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9a39b-120">Value</span></span>                     | <span data-ttu-id="9a39b-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a39b-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a39b-122">\_messaggio DSPROP ATTRCHANGED \_</span><span class="sxs-lookup"><span data-stu-id="9a39b-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="9a39b-123">"DsPropAttrChanged"</span><span class="sxs-lookup"><span data-stu-id="9a39b-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="9a39b-124">Messaggio inviato per sincronizzare le pagine delle proprietà e gli strumenti di amministrazione del servizio directory, dichiarati in DSClient. h.</span><span class="sxs-lookup"><span data-stu-id="9a39b-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="9a39b-125">GetClass DSQPM \_</span><span class="sxs-lookup"><span data-stu-id="9a39b-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="9a39b-126">CQPM \_ HANDLERSPECIFIC + 0</span><span class="sxs-lookup"><span data-stu-id="9a39b-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="9a39b-127">Messaggio di pagina inviato alle pagine del modulo per il recupero di un elenco di classi per la query, usato dal selettore dei campi e dalla proprietà per compilare l'elenco delle classi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a39b-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="9a39b-128">wParam = Flags e lParam = LPLPDSQUERYCLASSLIST, dichiarati in dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="9a39b-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="9a39b-129">\_HELPTOPICS DSQPM</span><span class="sxs-lookup"><span data-stu-id="9a39b-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="9a39b-130">(CQPM \_ HANDLERSPECIFIC + 1)</span><span class="sxs-lookup"><span data-stu-id="9a39b-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="9a39b-131">Un messaggio di pagina inviato alle pagine del modulo per la gestione della richiesta "argomenti della Guida".</span><span class="sxs-lookup"><span data-stu-id="9a39b-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="9a39b-132">wParam = 0, lParam = hWndParent, dichiarato in dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="9a39b-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




