---
title: Come usare le visualizzazioni affiancate
description: In questo argomento viene illustrato come impostare la visualizzazione affiancata per un controllo visualizzazione elenco.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963572"
---
# <a name="how-to-use-tile-views"></a>Come usare le visualizzazioni affiancate

In questo argomento viene illustrato come impostare la visualizzazione affiancata per un controllo visualizzazione elenco. Nella visualizzazione affiancata ogni elemento è rappresentato da un'icona grande con una o più righe di testo associato. Per un'illustrazione, vedere [informazioni sui controlli List-View](list-view-controls-overview.md).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Impostare i parametri di visualizzazione generali per la visualizzazione affiancata utilizzando la macro [**\_ SetTileViewInfo di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) . Utilizzare la struttura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) passata a questa macro per specificare la posizione del testo in relazione all'icona, le dimensioni di ogni riquadro (incluso il testo associato) e il numero massimo di righe di testo.

Se non si desidera che i riquadri vengano ridimensionati automaticamente, è necessario impostare **LVTVIF \_ FIXEDSIZE** nel membro **dwFlags** e **LVTVIM \_ TILESIZE** nel membro **dwMask** di [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), oltre a fornire le dimensioni nel membro **sizeTile** .

L'esempio di codice C++ seguente imposta le informazioni sulla visualizzazione affiancata per un controllo di visualizzazione elenco in modo da visualizzare un massimo di due elementi secondari per ogni elemento. Imposta anche le dimensioni di ogni sezione.


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



Per ogni elemento dell'elenco, è possibile impostare altri parametri quando l'elemento viene inserito nell'elenco o in un secondo momento. La struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) usata con [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contiene membri che specificano le colonne di dati da visualizzare sotto l'elemento e il relativo allineamento. Questi stessi parametri di visualizzazione sono disponibili anche nella struttura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) usata con [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).

> [!Note]  
> "Columns" si riferisce a non visualizzare le colonne nella visualizzazione affiancata, ma piuttosto agli elementi secondari, che vengono visualizzati in colonne nella visualizzazione dettagli.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo visualizzazione elenco](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni sui controlli List-View](list-view-controls-overview.md)
</dt> <dt>

[Uso di controlli List-View](using-list-view-controls.md)
</dt> </dl>

 

 




