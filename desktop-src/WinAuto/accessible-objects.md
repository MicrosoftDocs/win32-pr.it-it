---
title: Oggetti accessibili
description: Con Microsoft Active Accessibility, gli elementi dell'interfaccia utente vengono esposti ai client come oggetti Component Object Model (COM).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396815"
---
# <a name="accessible-objects"></a><span data-ttu-id="baaf8-103">Oggetti accessibili</span><span class="sxs-lookup"><span data-stu-id="baaf8-103">Accessible Objects</span></span>

<span data-ttu-id="baaf8-104">Con Microsoft Active Accessibility, gli elementi dell'interfaccia utente vengono esposti ai client come oggetti Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="baaf8-104">With Microsoft Active Accessibility, UI elements are exposed to clients as Component Object Model (COM) objects.</span></span> <span data-ttu-id="baaf8-105">Questi *oggetti accessibili* gestiscono informazioni, denominate *Proprietà*, che descrivono il nome dell'oggetto, la posizione dello schermo e altre informazioni necessarie per gli strumenti di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="baaf8-105">These *accessible objects* maintain pieces of information, called *properties*, which describe the object's name, screen location, and other information needed by accessibility aids.</span></span> <span data-ttu-id="baaf8-106">Gli oggetti accessibili forniscono anche *Metodi* che i client chiamano per provocare l'esecuzione di un'azione da parte dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="baaf8-106">Accessible objects also provide *methods* that clients call to cause the object to perform some action.</span></span> <span data-ttu-id="baaf8-107">Gli oggetti accessibili a cui sono associati elementi semplici sono denominati anche elementi *padre* o *contenitori*.</span><span class="sxs-lookup"><span data-stu-id="baaf8-107">Accessible objects that have simple elements associated with them are also called *parents*, or *containers*.</span></span>

<span data-ttu-id="baaf8-108">Gli oggetti accessibili vengono implementati utilizzando l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) basata su com di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="baaf8-108">Accessible objects are implemented using Microsoft Active Accessibility's COM-based [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="baaf8-109">I metodi e le proprietà **IAccessible** consentono alle applicazioni client di ottenere informazioni sugli elementi dell'interfaccia utente necessari per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="baaf8-109">The **IAccessible** methods and properties enable client applications to get information about UI elements needed by users.</span></span> <span data-ttu-id="baaf8-110">Ad esempio, [**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) restituisce un puntatore di interfaccia all'elemento padre di un oggetto accessibile e [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) consente ai client di ottenere informazioni su altri oggetti all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="baaf8-110">For example, [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) returns an interface pointer to an accessible object's parent, and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) provides a means for clients to get information about other objects within a container.</span></span>

<span data-ttu-id="baaf8-111">Per ulteriori informazioni sulla correlazione tra oggetti accessibili ed elementi semplici, vedere [elementi semplici](simple-elements.md).</span><span class="sxs-lookup"><span data-stu-id="baaf8-111">For more information about how accessible objects and simple elements are related, see [Simple Elements](simple-elements.md).</span></span>

 

 




