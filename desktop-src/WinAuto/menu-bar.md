---
title: Barra dei menu (riferimenti a elementi dell'interfaccia utente MSAA)
description: Una barra dei menu è l'area di una finestra immediatamente sotto la barra del titolo che contiene voci di menu quali File, Modifica, Finestra e Guida.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1212ba3c56673ab638e5aeedcc0ce20aea68dda2ad55e0904906d9f809c234ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998411"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barra dei menu (riferimenti a elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **barra dei menu** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti barra dei** menu in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Una barra dei menu è l'area di una finestra immediatamente sotto la barra del titolo che contiene voci di menu quali **File**, **Modifica**, **Finestra** e **Guida.** Microsoft Active Accessibility crea anche un oggetto barra dei menu per un menu di sistema, ovvero il menu nell'angolo superiore sinistro della barra del titolo e contiene voci di menu quali **Ripristina** **,** Sposta **,** Dimensioni **,** Riduci a icona e Ingrandisci . 

> [!Note]  
> Poiché i controlli barra dei menu non ricevono lo stato attivo, i metodi [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) non sono supportati per questo controllo.

 

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli barra dei menu supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli barra dei menu supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera [**l'oggetto IDispatch per**](idispatch-interface.md) la voce di menu specificata. Gli ID figlio per le voci di menu sono numerati in sequenza da sinistra a destra a partire da uno.                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è il numero di voci di menu nella barra dei menu. La **proprietà ChildCount** per un menu di sistema è una sola.                                                                                                                                                                                                                                                   |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | La **proprietà Description** per una barra dei menu è "Contiene i comandi per modificare la visualizzazione o il documento corrente". La **proprietà Description** per un menu di sistema è "Contains commands to manipulate the window".                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** per una barra dei menu sotto la barra del titolo è "ALT". La **proprietà KeyboardShortcut** per un menu di sistema è "ALT+BARRA SPAZIATRICE".                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** per una barra dei menu sotto la barra del titolo è "Application". La **proprietà Name** per un menu di sistema è "System".                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ MENUBAR.**](object-roles.md)                                                                                                                                                                                                                                                                                      |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

Il sistema attiva più di un evento [**\_ \_ MENUSTART DI SISTEMA EVENTI**](event-constants.md) che non ha sempre un evento [**\_ \_ MENUEND DI SISTEMA**](event-constants.md) EVENTI corrispondente. Inoltre, il sistema non attiva gli eventi [**\_ EVENT SYSTEM \_ MENUPOPUPSTART**](event-constants.md) e [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) in modo coerente. Si tratta di un problema noto che viene risolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Voce di menu**](menu-item.md)
</dt> <dt>

[**Menu a comparsa**](pop-up-menu.md)
</dt> </dl>

 

 





