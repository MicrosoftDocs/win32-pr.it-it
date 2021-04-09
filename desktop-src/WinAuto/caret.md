---
title: Accento circonflesso (riferimento all'elemento MSAA UI)
description: Il punto di inserimento è una linea lampeggiante, un blocco o una bitmap nell'area client di una finestra o in un controllo che accetta input da tastiera.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857945"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="ea408-103">Accento circonflesso (riferimento all'elemento MSAA UI)</span><span class="sxs-lookup"><span data-stu-id="ea408-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="ea408-104">Questo argomento descrive gli elementi di interesse per i riferimenti agli elementi dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="ea408-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="ea408-105">L'uso di un punto di inserimento in diversi framework dell'interfaccia utente non è descritto qui.</span><span class="sxs-lookup"><span data-stu-id="ea408-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="ea408-106">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="ea408-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="ea408-107">Il punto di inserimento è una linea lampeggiante, un blocco o una bitmap nell'area client di una finestra o in un controllo che accetta input da tastiera.</span><span class="sxs-lookup"><span data-stu-id="ea408-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="ea408-108">Indica la posizione in cui vengono inseriti testo o grafica.</span><span class="sxs-lookup"><span data-stu-id="ea408-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="ea408-109">Poiché solo una finestra alla volta ha lo stato attivo della tastiera, c'è un solo punto di inserimento nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ea408-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="ea408-110">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="ea408-110">IAccessible Methods</span></span>

<span data-ttu-id="ea408-111">Il punto di inserimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="ea408-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="ea408-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="ea408-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="ea408-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="ea408-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="ea408-114">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="ea408-114">IAccessible Properties</span></span>

<span data-ttu-id="ea408-115">Il punto di inserimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea408-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ea408-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ea408-116">Property</span></span></th>
<th><span data-ttu-id="ea408-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea408-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ea408-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea408-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="ea408-119">La proprietà <strong>childCount</strong> è zero.</span><span class="sxs-lookup"><span data-stu-id="ea408-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea408-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea408-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="ea408-121">La proprietà <strong>Name</strong> è &quot; Edit &quot; .</span><span class="sxs-lookup"><span data-stu-id="ea408-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ea408-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea408-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="ea408-123">La proprietà <strong>Role</strong> è <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea408-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ea408-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea408-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="ea408-125">I valori possibili per la proprietà <strong>state</strong> includono:</span><span class="sxs-lookup"><span data-stu-id="ea408-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="ea408-126">Zero, che indica che il punto di inserimento è visibile</span><span class="sxs-lookup"><span data-stu-id="ea408-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="ea408-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="ea408-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="ea408-128">Note</span><span class="sxs-lookup"><span data-stu-id="ea408-128">Notes</span></span>

-   <span data-ttu-id="ea408-129">A differenza di altri elementi dell'interfaccia utente, all'oggetto cursore non è associato un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="ea408-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="ea408-130">Per ottenere l'accesso all'oggetto del cursore, i client devono impostare un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e attendere che l'oggetto del cursore generi gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ea408-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="ea408-131">L'oggetto del punto di inserimento nel controllo Rich Edit fornito da Riched20.dll (usato negli editor di testo, ad esempio Microsoft WordPad in Windows 98), non invia alcun [winEvents](winevents-infrastructure.md) quando la relativa posizione viene modificata durante la selezione del testo.</span><span class="sxs-lookup"><span data-stu-id="ea408-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="ea408-132">Quando gli utenti preme MAIUSC e tasti di direzione per selezionare il testo, l'oggetto del cursore non attiva l' [**\_ oggetto evento \_ posizioneCambia**](event-constants.md) WinEvent.</span><span class="sxs-lookup"><span data-stu-id="ea408-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="ea408-133">Analogamente, quando la selezione viene impostata a livello di programmazione tramite messaggi Rich Edit, l'oggetto cursore non invia alcun evento per indicare la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="ea408-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="ea408-134">Tutte le applicazioni che utilizzano Riched20.dll presentano questo problema.</span><span class="sxs-lookup"><span data-stu-id="ea408-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="ea408-135">Le applicazioni che usano versioni precedenti del controllo Rich Edit inviano correttamente gli eventi in base alla selezione.</span><span class="sxs-lookup"><span data-stu-id="ea408-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea408-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea408-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea408-137">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="ea408-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




