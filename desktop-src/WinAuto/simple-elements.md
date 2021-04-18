---
title: Elementi semplici
description: Un elemento semplice è un elemento dell'interfaccia utente che condivide un oggetto IAccessible con altri elementi e si basa su tale oggetto IAccessible, in genere il padre, per esporre le relative proprietà.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298863"
---
# <a name="simple-elements"></a><span data-ttu-id="72a7e-103">Elementi semplici</span><span class="sxs-lookup"><span data-stu-id="72a7e-103">Simple Elements</span></span>

<span data-ttu-id="72a7e-104">Un *elemento semplice* è un elemento dell'interfaccia utente che condivide un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con altri elementi e si basa su tale oggetto **IAccessible** , in genere il padre, per esporre le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="72a7e-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="72a7e-105">Per distinguere tra gli elementi che condividono un oggetto **IAccessible** , il server assegna un identificatore figlio univoco positivo a ogni elemento semplice.</span><span class="sxs-lookup"><span data-stu-id="72a7e-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="72a7e-106">Questa assegnazione viene eseguita per ogni singola istanza, quindi gli ID devono essere univoci all'interno di tale contesto.</span><span class="sxs-lookup"><span data-stu-id="72a7e-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="72a7e-107">Molte implementazioni assegnano questi ID in sequenza, a partire da 1.</span><span class="sxs-lookup"><span data-stu-id="72a7e-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="72a7e-108">Questo schema non consente agli elementi semplici di avere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="72a7e-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="72a7e-109">Gli elementi semplici sono noti anche come *figli*.</span><span class="sxs-lookup"><span data-stu-id="72a7e-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="72a7e-110">Per essere identificato ed esposto in modo univoco, un elemento semplice richiede un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e un ID figlio.</span><span class="sxs-lookup"><span data-stu-id="72a7e-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="72a7e-111">Pertanto, quando si comunica con un oggetto **IAccessible** , i client devono fornire l'ID figlio appropriato.</span><span class="sxs-lookup"><span data-stu-id="72a7e-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="72a7e-112">Un identificatore speciale, **CHILDID \_ self**, può essere usato per fare riferimento all'oggetto accessibile, anziché a uno dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="72a7e-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="72a7e-113">L'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) condiviso tra gli elementi semplici corrisponde spesso a un oggetto padre comune nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="72a7e-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="72a7e-114">Ad esempio, le caselle di riepilogo sistema espongono un oggetto accessibile per la casella di riepilogo complessiva e gli elementi semplici per ogni elemento casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="72a7e-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="72a7e-115">In questo caso, l'oggetto **IAccessible** per la casella di riepilogo è anche il padre o il contenitore degli elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="72a7e-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="72a7e-116">Per ulteriori informazioni sugli oggetti accessibili, vedere [oggetti accessibili](accessible-objects.md).</span><span class="sxs-lookup"><span data-stu-id="72a7e-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 




