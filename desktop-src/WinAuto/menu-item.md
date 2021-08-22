---
title: Voce di menu (riferimento all'elemento dell'interfaccia utente MSAA)
description: Una voce di menu rappresenta una voce specifica in una barra dei menu o in un menu a comparsa.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b90162f386314ac495ed138ccf4d180d2f53b8b1e6126287c79a1d75d40be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644501"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Voce di menu (riferimento all'elemento dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Voce di menu** ai fini del riferimento agli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Voce di menu** in vari framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

Una voce di menu rappresenta una voce specifica in una barra dei menu o in un menu a comparsa. Ad esempio, Microsoft Active Accessibility un oggetto voce di menu per il menu **File** nella barra dei menu. Analogamente, Microsoft Active Accessibility un oggetto voce di menu per la **voce** di menu Apri **dal** menu a comparsa File.

Il nome della classe della finestra per una voce di menu è \# "32768".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una voce di menu supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Metodo                                                                    | Commenti                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Per le voci di menu dalla barra dei menu, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) visualizza o chiude il menu a seconda dello stato del menu. Per le voci di menu da un menu a comparsa, **accDoDefaultAction** fa clic sulla voce di menu per eseguire il comando di menu. |
| [**acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una voce di menu supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera [**l'interfaccia IDispatch**](idispatch-interface.md) nell'oggetto menu popup per questa voce.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è una per le voci di menu che visualizzano un menu o un sottomenu. in caso **contrario, la proprietà ChildCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **proprietà DefaultAction** per le voci di menu che visualizzano un menu o un sottomenu è "Apri" o "Chiudi" a seconda dello stato del menu. La **proprietà DefaultAction** per tutte le altre voci di menu è "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta della voce di menu, ovvero il carattere sottolineato nel testo del nome della voce di menu. Ad esempio, la **proprietà KeyboardShortcut** per la voce di menu File è "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** corrisponde al nome della voce di menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **proprietà Parent** è la barra dei menu o il menu a comparsa che contiene la voce di menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ MENUITEM.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) o una combinazione di uno o più dei valori seguenti: [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ CHECKED STATE**](object-state-constants.md) SYSTEM \| [**\_ \_ DEFAULT STATE**](object-state-constants.md) SYSTEM \| [**\_ \_ HOTTRACKED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

-   Se usato in una voce di menu, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) restituisce S OK, ma non riesce a eseguire l'azione se il carattere usato nel tasto di scelta è ?, !, @o qualsiasi altro carattere che richiede il tasto MAIUSC o un altro tasto di \_ modifica. Ciò si verifica anche nelle tastiere internazionali con un carattere tasto di scelta che richiede la pressione del tasto ALT GR.
-   Il [**metodo accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con [**SELFLAG \_ TAKEFOCUS**](selflag.md) non determina l'apertura o la chiusura di un menu a comparsa da parte di una voce di menu. I client usano [**il metodo accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) per aprire o chiudere un menu a comparsa.
-   Una voce della barra dei menu che non visualizza un menu a comparsa restituisce "Application" per la **proprietà Name** anziché il nome della voce di menu.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra dei menu**](menu-bar.md)
</dt> <dt>

[**Menu a comparsa**](pop-up-menu.md)
</dt> </dl>

 

 





