---
title: Uso di un progetto personalizzato
description: Questa sezione contiene esempi che illustrano come implementare un progetto personalizzato.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046366"
---
# <a name="using-custom-draw"></a><span data-ttu-id="781c3-103">Uso di un progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="781c3-103">Using Custom Draw</span></span>

<span data-ttu-id="781c3-104">Questa sezione contiene esempi che illustrano come implementare un progetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="781c3-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="781c3-105">Il frammento di codice seguente è una parte di un gestore di [**\_ notifiche WM**](wm-notify.md) che illustra come gestire le notifiche di estrazione personalizzate inviate a un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="781c3-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



<span data-ttu-id="781c3-106">La prima [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) ha il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) impostato su **CDDS \_ PrePaint**.</span><span class="sxs-lookup"><span data-stu-id="781c3-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="781c3-107">Il gestore restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) per indicare che desidera modificare uno o più elementi singolarmente.</span><span class="sxs-lookup"><span data-stu-id="781c3-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="781c3-108">Se nel passaggio precedente è stato restituito [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) , la notifica [di \_ CUSTOMDRAW di Nm](nm-customdraw.md) successiva ha **dwDrawStage** impostato su **CDDS \_ ITEMPREPAINT**.</span><span class="sxs-lookup"><span data-stu-id="781c3-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="781c3-109">Il gestore recupera il colore corrente e i valori del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="781c3-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="781c3-110">A questo punto, è possibile specificare nuovi valori per icone piccole, icone grandi e modalità elenco.</span><span class="sxs-lookup"><span data-stu-id="781c3-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="781c3-111">Se il controllo è in modalità report, è anche possibile specificare nuovi valori che verranno applicati a tutti gli elementi secondari dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="781c3-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="781c3-112">Se è stato modificato un valore, restituire [**CDRF \_ NEWFONT**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="781c3-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="781c3-113">Se il controllo è in modalità report e si desidera gestire singolarmente gli elementi secondari, restituire **CDRF \_ NOTIFYSUBITEMDRAW**.</span><span class="sxs-lookup"><span data-stu-id="781c3-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="781c3-114">La notifica finale viene inviata solo se il controllo è in modalità report ed è stato restituito **CDRF \_ NOTIFYSUBITEMDRAW** nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="781c3-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="781c3-115">La procedura per modificare i tipi di carattere e i colori è identica a quella del passaggio, ma si applica solo a un singolo elemento secondario.</span><span class="sxs-lookup"><span data-stu-id="781c3-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="781c3-116">Restituisce [**CDRF \_ NEWFONT**](cdrf-constants.md) per notificare al controllo se il colore o il tipo di carattere è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="781c3-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="781c3-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="781c3-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="781c3-118">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="781c3-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="781c3-119">Informazioni sul progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="781c3-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="781c3-120">Riferimento di progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="781c3-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="781c3-121">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="781c3-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="781c3-122">ESEMPIO: CustDTv illustra il progetto personalizzato in un oggetto TreeView (Q248496)</span><span class="sxs-lookup"><span data-stu-id="781c3-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




