---
title: Come usare i gruppi in un List-View
description: In questo argomento viene descritto come creare un'istanza di un gruppo e aggiungerla a un controllo visualizzazione elenco.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaad657d9ea6b71bac1d06a34a0aa29b99c26e204629e503a9e55531da162b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132121"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Come usare i gruppi in un List-View

In questo argomento viene descritto come creare un'istanza di un gruppo e aggiungerla a un controllo visualizzazione elenco. Il raggruppamento consente a un utente di disporre gli elenchi in gruppi di elementi divisi visivamente nella pagina, usando un divisore orizzontale e un titolo di gruppo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per usare i gruppi in un controllo visualizzazione elenco, assicurarsi che il controllo includa lo stile della finestra [**LVS \_ ALIGNTOP.**](list-view-window-styles.md)

Quando si aggiunge un elemento all'elenco, lo si assegna a un gruppo impostando il membro **iGroupId** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento sul valore del membro **iGroupId** della struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) dei gruppi. Un elemento non assegnato a un gruppo non viene visualizzato nell'elenco quando è abilitata la visualizzazione gruppo. Per abilitare o disabilitare la visualizzazione gruppo, usa la macro [**\_ ListView EnableGroupView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)

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

[Informazioni di riferimento sul controllo List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni List-View controlli](list-view-controls-overview.md)
</dt> <dt>

[Uso di List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 




