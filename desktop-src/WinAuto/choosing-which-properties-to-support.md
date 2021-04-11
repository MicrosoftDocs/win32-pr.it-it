---
title: Scelta delle proprietà da supportare
description: Le proprietà IAccessible forniscono agli sviluppatori di server un modo per descrivere un'ampia gamma di elementi dell'interfaccia utente.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330919"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="87279-103">Scelta delle proprietà da supportare</span><span class="sxs-lookup"><span data-stu-id="87279-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="87279-104">Le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) forniscono agli sviluppatori di server un modo per descrivere un'ampia gamma di elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="87279-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="87279-105">Tuttavia, non tutte le proprietà sono applicabili per ogni tipo di elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="87279-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="87279-106">Alcune proprietà, inoltre, forniscono informazioni descrittive utili ma non essenziali.</span><span class="sxs-lookup"><span data-stu-id="87279-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="87279-107">Per ogni oggetto è necessario che i server supportino le proprietà e i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="87279-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="87279-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="87279-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="87279-109">**Role**</span><span class="sxs-lookup"><span data-stu-id="87279-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="87279-110">**State**</span><span class="sxs-lookup"><span data-stu-id="87279-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="87279-111">[**Percorso**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="87279-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="87279-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="87279-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="87279-113">Le proprietà e il metodo seguenti devono essere supportati se sono applicabili all'oggetto:</span><span class="sxs-lookup"><span data-stu-id="87279-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="87279-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="87279-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="87279-115">**Valore**</span><span class="sxs-lookup"><span data-stu-id="87279-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="87279-116">Se l'oggetto dispone di elementi figlio, è necessario che le proprietà e il metodo seguenti siano supportati:</span><span class="sxs-lookup"><span data-stu-id="87279-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="87279-117">[**Figlio**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) e [ **childCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="87279-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="87279-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md)e [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="87279-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="87279-119">Le proprietà seguenti sono facoltative, ma forniscono utili informazioni descrittive sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="87279-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="87279-120">La proprietà [**Description**](description-property.md) viene implementata per descrivere le bitmap e altre immagini.</span><span class="sxs-lookup"><span data-stu-id="87279-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="87279-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="87279-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="87279-122">[**DefaultAction**](defaultaction-property.md) e [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="87279-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="87279-123">**Help**</span><span class="sxs-lookup"><span data-stu-id="87279-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="87279-124">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="87279-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




