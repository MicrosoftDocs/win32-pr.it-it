---
title: Voce di menu (riferimento all'elemento MSAA UI)
description: Una voce di menu rappresenta un particolare elemento in una barra dei menu o un menu a comparsa.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb6621a14927cc4dc9af9f3384157e60ce6570d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044916"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Voce di menu (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **voce di menu** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti **voce di menu** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Una voce di menu rappresenta un particolare elemento in una barra dei menu o un menu a comparsa. Ad esempio, in Microsoft Active Accessibility viene creato un oggetto voce di menu per il menu **file** nella barra dei menu. Analogamente, Microsoft Active Accessibility crea un oggetto voce di menu per la voce di menu **Apri** dal menu di scelta rapida del **file** .

Il nome della classe della finestra per una voce di menu è " \# 32768".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una voce di menu supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Per le voci di menu della barra dei menu, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) Visualizza o chiude il menu a seconda dello stato del menu. Per le voci di menu da un menu a comparsa, **accDoDefaultAction** fa clic sulla voce di menu per eseguire il comando di menu. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una voce di menu supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Recupera l'interfaccia [**IDispatch**](idispatch-interface.md) nell'oggetto menu di scelta rapida per questo elemento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Il valore della proprietà **childCount** è uno per le voci di menu che visualizzano un menu o un sottomenu; in caso contrario, la proprietà **childCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La proprietà **DefaultAction** per le voci di menu che visualizzano un menu o un sottomenu può essere "Open" o "close" a seconda dello stato del menu. La proprietà **DefaultAction** per tutte le altre voci di menu è "Execute".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso della voce di menu, ovvero il carattere sottolineato nel testo del nome della voce di menu. Ad esempio, la proprietà **KeyboardShortcut** per la voce di menu file è "f".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** corrisponde al nome della voce di menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è la barra dei menu o il menu a comparsa che contiene la voce di menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è l'oggetto [**\_ \_ MenuItem del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è [**\_ \_ invisibile al sistema di stato**](object-state-constants.md) o una combinazione di uno o più dei valori seguenti: [**stato sistema non \_ \_ disponibile**](object-state-constants.md) sistema stato \| [**\_ \_ selezionato**](object-state-constants.md) stato sistema stato di sistema \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ HOTTRACKED**](object-state-constants.md) stato sistema stato \| [**\_ \_ attivo**](object-state-constants.md) sistema stato \| [**\_ \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

-   Quando viene usato in una voce di menu, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) restituisce S \_ OK, ma non riesce a eseguire l'azione se il carattere usato nella chiave di accesso è?,!, @ o qualsiasi altro carattere che richiede il tasto MAIUSC o un altro tasto di modifica. Questa situazione si verifica anche nelle tastiere internazionali con un carattere di chiave di accesso che richiede la pressione del tasto ALT GR.
-   Il metodo [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con [**SELFLAG \_ TAKEFOCUS**](selflag.md) non determina l'apertura o la chiusura di un menu a comparsa di una voce di menu. I client usano il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) per aprire o chiudere un menu a comparsa.
-   Una voce della barra dei menu che non visualizza un menu a comparsa restituisce "Application" per la proprietà **Name** anziché il nome della voce di menu.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barra dei menu**](menu-bar.md)
</dt> <dt>

[**Menu a comparsa**](pop-up-menu.md)
</dt> </dl>

 

 





