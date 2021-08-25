---
title: Menu a comparsa (riferimenti a elementi dell'interfaccia utente MSAA)
description: Un menu a comparsa visualizza un elenco di comandi di menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b578a6af66585e06c4d9392f7051a8ebf14c8c24865bac59bf0c4fa43c7deaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861391"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menu a comparsa (riferimenti a elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli **oggetti menu a comparsa** ai fini delle informazioni di riferimento sugli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Menu a comparsa** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Un menu a comparsa visualizza un elenco di comandi di menu. Microsoft Active Accessibility crea un oggetto popup di menu quando viene aperta una voce di menu in una barra dei menu. Microsoft Active Accessibility crea anche oggetti popup di menu per i menu di scelta rapida, che vengono visualizzati quando l'utente fa clic con il pulsante destro del mouse su un elemento dell'interfaccia utente.

Il nome della classe della finestra per un menu a comparsa è " \# 32768".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un menu a comparsa supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un menu a comparsa supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Recupera [**l'oggetto IDispatch per**](idispatch-interface.md) la voce di menu specificata. Gli ID figlio per le voci di menu sono numerati in sequenza dall'alto verso il basso a partire da uno.                                                                                                                                                                                                                                                                                      |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **proprietà ChildCount** è il numero di voci di menu nel menu, inclusi i separatori di menu.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **proprietà** Name per un menu a comparsa ha lo stesso nome del menu. La **proprietà Name** per un menu di scelta rapida è "Context".                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **proprietà Parent** è una finestra ( ROLE SYSTEM [**\_ \_ WINDOW**](object-roles.md) ) che racchiude il menu a comparsa e ha lo stesso nome della proprietà **Name** e della classe della finestra del menu a comparsa .                                                                                                                                                                                                                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **proprietà Role** è ROLE SYSTEM [**\_ \_ MENUPOPUP.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

-   Gli oggetti del menu a comparsa non attivano [**eventi EVENT \_ OBJECT \_ CREATE**](event-constants.md) e [**EVENT OBJECT \_ \_ DESTROY.**](event-constants.md)
-   I menu a più colonne non supportano i flag [**NAVDIR \_ LEFT**](navigation-constants.md) o [**NAVDIR \_ RIGHT**](navigation-constants.md) del [**metodo accNavigate.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   Gli eventi [**EVENT \_ SYSTEM \_ MENUPOPUPSTART**](event-constants.md) e [**EVENT SYSTEM \_ \_ MENUPOPUPEND**](event-constants.md) non vengono inviati in modo coerente. Si tratta di un problema noto che viene risolto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra dei menu**](menu-bar.md)
</dt> <dt>

[**Voce di menu**](menu-item.md)
</dt> </dl>

 

 





