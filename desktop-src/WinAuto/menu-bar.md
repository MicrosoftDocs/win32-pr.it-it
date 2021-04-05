---
title: Barra dei menu (riferimento all'elemento dell'interfaccia utente MSAA)
description: Una barra dei menu è l'area di una finestra immediatamente sotto la barra del titolo che contiene voci di menu, ad esempio file, modifica, finestra e guida.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515763"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barra dei menu (riferimento all'elemento dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti della **barra dei menu** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti della **barra dei menu** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Una barra dei menu è l'area di una finestra immediatamente sotto la barra del titolo che contiene voci di menu, ad esempio **file**, **modifica**, **finestra** e **Guida**. Microsoft Active Accessibility crea anche un oggetto barra dei menu per un menu di sistema, che è il menu nell'angolo superiore sinistro della barra del titolo e contiene voci di menu quali **Restore**, **Move**, **size**, **minimizzate** e **ingrandire**.

> [!Note]  
> Poiché i controlli barra dei menu non ricevono lo stato attivo, i metodi [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) non sono supportati per questo controllo.

 

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli barra dei menu supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli barra dei menu supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera il [**IDispatch**](idispatch-interface.md) per la voce di menu specificata. Gli ID figlio per le voci di menu sono numerati in sequenza da sinistra a destra a partire da uno.                                                                                                                                                                                             |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è il numero di voci di menu sulla barra dei menu. La proprietà **childCount** per un menu di sistema è uno.                                                                                                                                                                                                                                                   |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | La proprietà **Description** per una barra dei menu è "contiene i comandi per la modifica della vista o del documento corrente". La proprietà **Description** per un menu di sistema è "contiene i comandi per la modifica della finestra".                                                                                                                                                                   |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** per una barra dei menu sotto la barra del titolo è "Alt". La proprietà **KeyboardShortcut** per un menu di sistema è "ALT + barra spaziatrice".                                                                                                                                                                                                                             |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** per una barra dei menu sotto la barra del titolo è "Application". La proprietà **Name** di un menu di sistema è "System".                                                                                                                                                                                                                                                |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è la [**barra dei \_ \_ menu del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato del sistema stato [**\_ \_**](object-state-constants.md) \| [**\_ \_ incentrato**](object-state-constants.md) sullo stato di sistema stato \| [**\_ \_ inattivo**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

Il sistema attiva più di un [**evento \_ \_ l'MenuStart del sistema di eventi**](event-constants.md) che non ha sempre un evento [**\_ \_ MENUEND del sistema di eventi**](event-constants.md) corrispondente. Inoltre, il sistema non attiva in modo coerente gli eventi [**\_ \_ MENUPOPUPSTART**](event-constants.md) e [**\_ \_ MENUPOPUPEND**](event-constants.md) del sistema di eventi. Si tratta di un problema noto che viene risolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Voce di menu**](menu-item.md)
</dt> <dt>

[**Menu a comparsa**](pop-up-menu.md)
</dt> </dl>

 

 





