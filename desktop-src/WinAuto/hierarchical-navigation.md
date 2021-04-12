---
title: Navigazione gerarchica
description: Spesso i client devono spostarsi tra gli oggetti in base alle relazioni padre-figlio. Ad esempio, un client potrebbe avere già informazioni su un controllo della barra degli strumenti, ma non avere informazioni sui pulsanti in esso contenuti.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221409"
---
# <a name="hierarchical-navigation"></a><span data-ttu-id="ff990-104">Navigazione gerarchica</span><span class="sxs-lookup"><span data-stu-id="ff990-104">Hierarchical Navigation</span></span>

<span data-ttu-id="ff990-105">Spesso i client devono spostarsi tra gli oggetti in base alle relazioni padre-figlio.</span><span class="sxs-lookup"><span data-stu-id="ff990-105">Often clients must move between objects based on their parent-child relationships.</span></span> <span data-ttu-id="ff990-106">Ad esempio, un client potrebbe avere già informazioni su un controllo della barra degli strumenti, ma non avere informazioni sui pulsanti in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="ff990-106">For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.</span></span>

<span data-ttu-id="ff990-107">L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) espone le relazioni gerarchiche tra gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="ff990-107">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface exposes the hierarchical relationships between objects.</span></span> <span data-ttu-id="ff990-108">I client possono passare da un oggetto padre ai relativi elementi figlio o da un oggetto figlio al relativo padre chiamando [**IAccessible:: Get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) o [**IAccessible:: Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span><span class="sxs-lookup"><span data-stu-id="ff990-108">Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) or [**IAccessible::get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span></span>

 

 




