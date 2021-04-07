---
title: Come usare i gruppi in un List-View
description: In questo argomento viene descritto come creare un'istanza di un gruppo e aggiungerla a un controllo visualizzazione elenco.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873126"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Come usare i gruppi in un List-View

In questo argomento viene descritto come creare un'istanza di un gruppo e aggiungerla a un controllo visualizzazione elenco. Il raggruppamento consente a un utente di disporre gli elenchi in gruppi di elementi che sono divisi visivamente nella pagina, usando un separatore orizzontale e un titolo di gruppo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Per usare i gruppi in un controllo visualizzazione elenco, verificare che il controllo includa lo stile della finestra [**\_ ALIGNTOP di LVS**](list-view-window-styles.md) .

Quando si aggiunge un elemento all'elenco, lo si assegna a un gruppo impostando il membro **iGroupId** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento sul valore del membro **iGroupId** della struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) del gruppo. Un elemento non assegnato a un gruppo non viene visualizzato nell'elenco quando è abilitata la visualizzazione gruppo. Per abilitare o disabilitare la visualizzazione dei gruppi, usare la macro [**\_ EnableGroupView di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .

Nell'esempio seguente viene illustrato come creare un gruppo con un'intestazione e aggiungerlo a un controllo di visualizzazione elenco.


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo visualizzazione elenco](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni sui controlli List-View](list-view-controls-overview.md)
</dt> <dt>

[Uso di controlli List-View](using-list-view-controls.md)
</dt> </dl>

 

 




