---
title: Uso del disegno personalizzato
description: Questa sezione contiene esempi che illustrano come implementare il disegno personalizzato.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90cff5fd4d692d31b69c85980f872f3aca4504cad81a3439d0c4d31a4c73d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655871"
---
# <a name="using-custom-draw"></a>Uso del disegno personalizzato

Questa sezione contiene esempi che illustrano come implementare il disegno personalizzato.

Il frammento di codice seguente è una parte di un gestore [**WM \_ NOTIFY**](wm-notify.md) che illustra come gestire le notifiche di disegno personalizzate inviate a un controllo visualizzazione elenco.


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



La prima [notifica DI NM \_ CUSTOMDRAW](nm-customdraw.md) ha il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) impostato su **CDDS \_ PREPAINT**. Il gestore restituisce [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) per indicare che desidera modificare singolarmente uno o più elementi.

Se nel passaggio precedente è stato restituito [**CDRF \_ NOTIFYITEMDRAW,**](cdrf-constants.md) la notifica [NM \_ CUSTOMDRAW](nm-customdraw.md) successiva ha **dwDrawStage** impostato su **CDDS \_ ITEMPREPAINT**. Il gestore recupera il colore e i valori del carattere correnti. A questo punto, è possibile specificare nuovi valori per le modalità icona piccola, icona grande ed elenco. Se il controllo è in modalità report, è anche possibile specificare nuovi valori che verranno applicati a tutti gli elementi secondari dell'elemento. Se sono state modificate modifiche, restituire [**CDRF \_ NEWFONT**](cdrf-constants.md). Se il controllo è in modalità report e si desidera gestire singolarmente gli elementi secondari, restituire **CDRF \_ NOTIFYSUBITEMDRAW**.

La notifica finale viene inviata solo se il controllo è in modalità report ed è stato restituito **CDRF \_ NOTIFYSUBITEMDRAW** nel passaggio precedente. La procedura per la modifica di tipi di carattere e colori è la stessa di tale passaggio, ma si applica solo a un singolo elemento secondario. Restituisce [**CDRF \_ NEWFONT**](cdrf-constants.md) per notificare al controllo se il colore o il tipo di carattere è stato modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sul disegno personalizzato](about-custom-draw.md)
</dt> <dt>

[Informazioni di riferimento sul disegno personalizzato](custom-draw-reference.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[ESEMPIO: CustDTv illustra il disegno personalizzato in un controllo TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




