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
# <a name="using-custom-draw"></a>Uso di un progetto personalizzato

Questa sezione contiene esempi che illustrano come implementare un progetto personalizzato.

Il frammento di codice seguente è una parte di un gestore di [**\_ notifiche WM**](wm-notify.md) che illustra come gestire le notifiche di estrazione personalizzate inviate a un controllo di visualizzazione elenco.


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



La prima [notifica \_ CUSTOMDRAW di Nm](nm-customdraw.md) ha il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) impostato su **CDDS \_ PrePaint**. Il gestore restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) per indicare che desidera modificare uno o più elementi singolarmente.

Se nel passaggio precedente è stato restituito [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) , la notifica [di \_ CUSTOMDRAW di Nm](nm-customdraw.md) successiva ha **dwDrawStage** impostato su **CDDS \_ ITEMPREPAINT**. Il gestore recupera il colore corrente e i valori del tipo di carattere. A questo punto, è possibile specificare nuovi valori per icone piccole, icone grandi e modalità elenco. Se il controllo è in modalità report, è anche possibile specificare nuovi valori che verranno applicati a tutti gli elementi secondari dell'elemento. Se è stato modificato un valore, restituire [**CDRF \_ NEWFONT**](cdrf-constants.md). Se il controllo è in modalità report e si desidera gestire singolarmente gli elementi secondari, restituire **CDRF \_ NOTIFYSUBITEMDRAW**.

La notifica finale viene inviata solo se il controllo è in modalità report ed è stato restituito **CDRF \_ NOTIFYSUBITEMDRAW** nel passaggio precedente. La procedura per modificare i tipi di carattere e i colori è identica a quella del passaggio, ma si applica solo a un singolo elemento secondario. Restituisce [**CDRF \_ NEWFONT**](cdrf-constants.md) per notificare al controllo se il colore o il tipo di carattere è stato modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sul progetto personalizzato](about-custom-draw.md)
</dt> <dt>

[Riferimento di progetto personalizzato](custom-draw-reference.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[ESEMPIO: CustDTv illustra il progetto personalizzato in un oggetto TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




