---
title: Proprietà e metodi di navigazione degli oggetti
description: I client passano da un oggetto all'altro usando metodi quali IAccessible accNavigate e IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955367"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="15c75-103">Proprietà e metodi di navigazione degli oggetti</span><span class="sxs-lookup"><span data-stu-id="15c75-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="15c75-104">I client *passano* da un oggetto all'altro usando metodi quali [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span><span class="sxs-lookup"><span data-stu-id="15c75-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="15c75-105">Questi metodi consentono ai client di recuperare un ID figlio o l'indirizzo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) di un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="15c75-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="15c75-106">La navigazione consente ai client di esplorare il modo in cui gli oggetti sono correlati tra loro.</span><span class="sxs-lookup"><span data-stu-id="15c75-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="15c75-107">Si noti che la navigazione verso un altro oggetto non modifica la selezione o lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="15c75-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="15c75-108">L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornisce proprietà e metodi che supportano i tipi di navigazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="15c75-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="15c75-109">Navigazione gerarchica</span><span class="sxs-lookup"><span data-stu-id="15c75-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="15c75-110">Navigazione spaziale e logica</span><span class="sxs-lookup"><span data-stu-id="15c75-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="15c75-111">Navigazione tramite hit testing e posizione dello schermo</span><span class="sxs-lookup"><span data-stu-id="15c75-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 




