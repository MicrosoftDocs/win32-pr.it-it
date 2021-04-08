---
title: Menu a comparsa (riferimento all'elemento dell'interfaccia utente MSAA)
description: Un menu a comparsa Visualizza un elenco di comandi di menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856497"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menu a comparsa (riferimento all'elemento dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **menu popup** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **menu popup** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Un menu a comparsa Visualizza un elenco di comandi di menu. Microsoft Active Accessibility crea un oggetto popup del menu quando viene aperta una voce di menu in una barra dei menu. Microsoft Active Accessibility crea anche oggetti popup del menu per i menu di scelta rapida, che vengono visualizzati quando l'utente fa clic con il pulsante destro del mouse su un elemento dell'interfaccia utente.

Il nome della classe della finestra per un menu di scelta rapida è " \# 32768".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un menu popup supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un menu popup supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Recupera il [**IDispatch**](idispatch-interface.md) per la voce di menu specificata. Gli ID figlio per le voci di menu sono numerati in sequenza dall'alto verso il basso iniziando da uno.                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La proprietà **childCount** è il numero di voci di menu nel menu, inclusi i separatori di menu.                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La proprietà **Name** di un menu di scelta rapida corrisponde al nome del menu. La proprietà **Name** di un menu di scelta rapida è "context".                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il menu di scelta rapida e ha la stessa proprietà **Name** e il nome della classe di finestra del menu a comparsa.                                                                                                                                                                                                                                                      |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La proprietà **Role** è [**\_ \_ MENUPOPUP del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="notes"></a>Note

-   Gli oggetti menu popup non attivano gli eventi di [**\_ \_ creazione**](event-constants.md) di oggetti evento e [**\_ \_ eliminazione di oggetti evento**](event-constants.md) .
-   I menu a più colonne non supportano i flag [**NAVDIR \_ Left**](navigation-constants.md) o [**NAVDIR \_ right**](navigation-constants.md) del metodo [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .
-   Gli eventi [**\_ \_ MENUPOPUPSTART**](event-constants.md) e [**\_ \_ MENUPOPUPEND**](event-constants.md) del sistema eventi non vengono inviati in modo coerente. Si tratta di un problema noto che viene risolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra dei menu**](menu-bar.md)
</dt> <dt>

[**Voce di menu**](menu-item.md)
</dt> </dl>

 

 





