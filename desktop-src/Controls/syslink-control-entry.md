---
title: SysLink
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli SysLink.
ms.assetid: 13a7b6d0-4bf1-480f-b447-838a550a5866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9bbfaea9b86c2d8dc42c84d050e5bec997ceb18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955310"
---
# <a name="syslink"></a><span data-ttu-id="d7172-103">SysLink</span><span class="sxs-lookup"><span data-stu-id="d7172-103">SysLink</span></span>

<span data-ttu-id="d7172-104">Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli SysLink.</span><span class="sxs-lookup"><span data-stu-id="d7172-104">This section contains information about the programming elements used with SysLink controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="d7172-105">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="d7172-105">Overviews</span></span>



| <span data-ttu-id="d7172-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="d7172-106">Topic</span></span>                                    | <span data-ttu-id="d7172-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="d7172-107">Contents</span></span>                                                                                       |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7172-108">Controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="d7172-108">SysLink Controls</span></span>](syslink-overview.md) | <span data-ttu-id="d7172-109">Il controllo SysLink rappresenta un modo pratico per incorporare collegamenti ipertestuali in una finestra.</span><span class="sxs-lookup"><span data-stu-id="d7172-109">The SysLink control provides a convenient way to embed hypertext links in a window.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="d7172-110">Messaggi</span><span class="sxs-lookup"><span data-stu-id="d7172-110">Messages</span></span>



| <span data-ttu-id="d7172-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="d7172-111">Topic</span></span>                                           | <span data-ttu-id="d7172-112">Contenuto</span><span class="sxs-lookup"><span data-stu-id="d7172-112">Contents</span></span>                                                                             |
|-------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7172-113">**\_GETIDEALHEIGHT LM**</span><span class="sxs-lookup"><span data-stu-id="d7172-113">**LM\_GETIDEALHEIGHT**</span></span>](lm-getidealheight.md) | <span data-ttu-id="d7172-114">Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="d7172-114">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="d7172-115">**\_GETIDEALSIZE LM**</span><span class="sxs-lookup"><span data-stu-id="d7172-115">**LM\_GETIDEALSIZE**</span></span>](lm-getidealsize.md)     | <span data-ttu-id="d7172-116">Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="d7172-116">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="d7172-117">**GetItem di LM \_**</span><span class="sxs-lookup"><span data-stu-id="d7172-117">**LM\_GETITEM**</span></span>](lm-getitem.md)               | <span data-ttu-id="d7172-118">Recupera gli Stati e gli attributi di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7172-118">Retrieves the states and attributes of an item.</span></span><br/>                           |
| [<span data-ttu-id="d7172-119">**HITTEST di LM \_**</span><span class="sxs-lookup"><span data-stu-id="d7172-119">**LM\_HITTEST**</span></span>](lm-hittest.md)               | <span data-ttu-id="d7172-120">Determina se l'utente ha fatto clic sul collegamento specificato.</span><span class="sxs-lookup"><span data-stu-id="d7172-120">Determines whether the user clicked the specified link.</span></span><br/>                   |
| [<span data-ttu-id="d7172-121">**\_elemento GETitem**</span><span class="sxs-lookup"><span data-stu-id="d7172-121">**LM\_SETITEM**</span></span>](lm-setitem.md)               | <span data-ttu-id="d7172-122">Imposta gli Stati e gli attributi di un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7172-122">Sets the states and attributes of an item.</span></span><br/>                                |



 

### <a name="structures"></a><span data-ttu-id="d7172-123">Strutture</span><span class="sxs-lookup"><span data-stu-id="d7172-123">Structures</span></span>



| <span data-ttu-id="d7172-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="d7172-124">Topic</span></span>                                | <span data-ttu-id="d7172-125">Contenuto</span><span class="sxs-lookup"><span data-stu-id="d7172-125">Contents</span></span>                                                                                                                                                                           |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7172-126">**LHITTESTINFO**</span><span class="sxs-lookup"><span data-stu-id="d7172-126">**LHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lhittestinfo) | <span data-ttu-id="d7172-127">Utilizzato per ottenere informazioni sul collegamento corrispondente a una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="d7172-127">Used to get information about the link corresponding to a given location.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="d7172-128">**LITEM**</span><span class="sxs-lookup"><span data-stu-id="d7172-128">**LITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-litem)               | <span data-ttu-id="d7172-129">Utilizzato per impostare e recuperare le informazioni su un elemento di collegamento.</span><span class="sxs-lookup"><span data-stu-id="d7172-129">Used to set and retrieve information about a link item.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="d7172-130">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="d7172-130">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)             | <span data-ttu-id="d7172-131">[**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) contiene informazioni di notifica.</span><span class="sxs-lookup"><span data-stu-id="d7172-131">The [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) Contains notification information.</span></span> <span data-ttu-id="d7172-132">Inviare questa struttura con i messaggi di risposta [nm \_ Click](nm-click-syslink.md) o [nm \_ ](nm-return.md) .</span><span class="sxs-lookup"><span data-stu-id="d7172-132">Send this structure with the [NM\_CLICK](nm-click-syslink.md) or [NM\_RETURN](nm-return.md) messages.</span></span><br/> |



 

 

 





