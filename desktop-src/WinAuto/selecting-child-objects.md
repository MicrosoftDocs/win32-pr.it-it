---
title: Selezione di oggetti figlio
description: I client chiamano il metodo IAccessible accSelect per modificare la selezione o lo stato attivo della tastiera tra gli elementi figlio di un oggetto. Le costanti SELFLAG specificate con la chiamata definiscono l'operazione da eseguire.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328911"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="1acf2-104">Selezione di oggetti figlio</span><span class="sxs-lookup"><span data-stu-id="1acf2-104">Selecting Child Objects</span></span>

<span data-ttu-id="1acf2-105">I client chiamano il metodo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) per modificare la selezione o lo stato attivo della tastiera tra gli elementi figlio di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1acf2-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="1acf2-106">Le [costanti SELFLAG](selflag.md) specificate con la chiamata definiscono l'operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="1acf2-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="1acf2-107">Se [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) viene chiamato con il flag [**SELFLAG \_ TAKEFOCUS**](selflag.md) su un oggetto figlio con **HWND**, il flag viene applicato solo se l'elemento padre dell'oggetto ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="1acf2-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="1acf2-108">Esecuzione di operazioni di selezione complesse</span><span class="sxs-lookup"><span data-stu-id="1acf2-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="1acf2-109">Di seguito vengono descritti i valori SELFLAG da specificare quando si chiama [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) per eseguire operazioni di selezione complesse.</span><span class="sxs-lookup"><span data-stu-id="1acf2-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="1acf2-110">**Per simulare un clic**</span><span class="sxs-lookup"><span data-stu-id="1acf2-110">**To simulate a click**</span></span>

-   <span data-ttu-id="1acf2-111">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="1acf2-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="1acf2-112">**Per selezionare un elemento di destinazione simulando CTRL + clic**</span><span class="sxs-lookup"><span data-stu-id="1acf2-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="1acf2-113">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="1acf2-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="1acf2-114">**Per annullare la selezione di un elemento di destinazione simulando CTRL + clic**</span><span class="sxs-lookup"><span data-stu-id="1acf2-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="1acf2-115">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="1acf2-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="1acf2-116">**Per simulare MAIUSC + clic**</span><span class="sxs-lookup"><span data-stu-id="1acf2-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="1acf2-117">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="1acf2-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="1acf2-118">**Per selezionare un intervallo di oggetti e impostare lo stato attivo sull'ultimo oggetto**</span><span class="sxs-lookup"><span data-stu-id="1acf2-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="1acf2-119">Specificare [**SELFLAG \_ TAKEFOCUS**](selflag.md) nell'oggetto iniziale per impostare l'ancoraggio di selezione.</span><span class="sxs-lookup"><span data-stu-id="1acf2-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="1acf2-120">Chiamare di nuovo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e specificare [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) sull'ultimo oggetto.</span><span class="sxs-lookup"><span data-stu-id="1acf2-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="1acf2-121">**Per deselezionare tutti gli oggetti**</span><span class="sxs-lookup"><span data-stu-id="1acf2-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="1acf2-122">Specificare [**SELFLAG \_ TAKESELECTION**](selflag.md) in qualsiasi oggetto.</span><span class="sxs-lookup"><span data-stu-id="1acf2-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="1acf2-123">Questo flag deseleziona tutti gli oggetti selezionati eccetto quello appena selezionato.</span><span class="sxs-lookup"><span data-stu-id="1acf2-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="1acf2-124">Chiamare di nuovo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e specificare [**SELFLAG \_ REMOVESELECTION**](selflag.md) nell'oggetto rimanente.</span><span class="sxs-lookup"><span data-stu-id="1acf2-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




