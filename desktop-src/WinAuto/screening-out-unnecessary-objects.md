---
title: Selezione di oggetti non necessari
description: Se si usa ispeziona per esaminare un semplice controllo, ad esempio un pulsante OK nell'accessorio Microsoft WordPad, è possibile osservare che questi oggetti finestra padre contengono anche diversi oggetti figlio invisibili.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297901"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="64011-103">Selezione di oggetti non necessari</span><span class="sxs-lookup"><span data-stu-id="64011-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="64011-104">Se si usa [ispeziona](inspect-objects.md) per esaminare un semplice controllo, ad esempio un pulsante OK nell'accessorio Microsoft WordPad, è possibile osservare che questi oggetti finestra padre contengono anche diversi oggetti figlio invisibili.</span><span class="sxs-lookup"><span data-stu-id="64011-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="64011-105">Questi oggetti invisibili hanno lo stesso nome della classe finestra del controllo e hanno la [proprietà state](state-property.md) del [**sistema di stato \_ \_ invisibile**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="64011-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="64011-106">Nella tabella seguente sono elencati gli oggetti figlio invisibili creati da Microsoft Active Accessibility per il controllo.</span><span class="sxs-lookup"><span data-stu-id="64011-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="64011-107">Nome</span><span class="sxs-lookup"><span data-stu-id="64011-107">Name</span></span>          | <span data-ttu-id="64011-108">Ruolo</span><span class="sxs-lookup"><span data-stu-id="64011-108">Role</span></span>                                                                  | <span data-ttu-id="64011-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="64011-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="64011-110">Sistema</span><span class="sxs-lookup"><span data-stu-id="64011-110">"System"</span></span>      | [<span data-ttu-id="64011-111">**\_barra dei \_ menu sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="64011-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="64011-112">0</span><span class="sxs-lookup"><span data-stu-id="64011-112">0</span></span>          |
| <span data-ttu-id="64011-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="64011-113">None</span></span>          | [<span data-ttu-id="64011-114">**barra di titolo \_ sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="64011-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="64011-115">5</span><span class="sxs-lookup"><span data-stu-id="64011-115">5</span></span>          |
| <span data-ttu-id="64011-116">Applicazione</span><span class="sxs-lookup"><span data-stu-id="64011-116">"Application"</span></span> | [<span data-ttu-id="64011-117">**\_barra dei \_ menu sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="64011-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="64011-118">0</span><span class="sxs-lookup"><span data-stu-id="64011-118">0</span></span>          |
| <span data-ttu-id="64011-119">Verticale</span><span class="sxs-lookup"><span data-stu-id="64011-119">"Vertical"</span></span>    | [<span data-ttu-id="64011-120">**\_barra di \_ scorrimento sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="64011-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="64011-121">5</span><span class="sxs-lookup"><span data-stu-id="64011-121">5</span></span>          |
| <span data-ttu-id="64011-122">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="64011-122">"Horizontal"</span></span>  | [<span data-ttu-id="64011-123">**\_barra di \_ scorrimento sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="64011-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="64011-124">5</span><span class="sxs-lookup"><span data-stu-id="64011-124">5</span></span>          |
| <span data-ttu-id="64011-125">"Casella dimensioni"</span><span class="sxs-lookup"><span data-stu-id="64011-125">"Size Box"</span></span>    | [<span data-ttu-id="64011-126">**\_grip sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="64011-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="64011-127">0</span><span class="sxs-lookup"><span data-stu-id="64011-127">0</span></span>          |



 

<span data-ttu-id="64011-128">Gli sviluppatori client devono identificare e filtrare gli oggetti finestra padre e gli oggetti figlio invisibili perché non forniscono informazioni significative agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="64011-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




