---
title: Pulsante push (riferimento all'elemento dell'interfaccia utente MSAA)
description: Un pulsante di pressione è un piccolo oggetto rettangolare usato per eseguire un'azione. Ad esempio, i pulsanti OK e ANNULLA in una finestra di dialogo sono pulsanti push.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4056b1b2bd8f80e79916db0056de176962bd7d3d86c2b62420deaf57f90e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644491"
---
# <a name="push-button-msaa-ui-element-reference"></a>Pulsante push (riferimento all'elemento dell'interfaccia utente MSAA)

Un pulsante di pressione è un piccolo oggetto rettangolare usato per eseguire un'azione. Ad esempio, i **pulsanti OK** **e ANNULLA** in una finestra di dialogo sono pulsanti push.

Il nome della classe della finestra per un pulsante push è "BUTTON".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un pulsante push supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Metodo                                                                    | Commenti                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Il [**metodo accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) fa clic sul pulsante push. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un pulsante push supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è zero o più.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **proprietà DefaultAction** è "Press".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta del pulsante, ovvero un carattere sottolineato nel testo del testo della finestra del pulsante. Ad esempio, "ALT+o" è la **proprietà KeyboardShortcut** per un **pulsante OK.**                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** viene ottenuta dal testo (o didascalia) della finestra del controllo, visualizzato nel pulsante di pressione. Ad esempio, "OK" è la **proprietà Name** per un **pulsante OK.**                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ PUSHBUTTON**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE STATE**](object-state-constants.md) SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PRESSED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ DEFAULT**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casella di controllo**](check-box.md)
</dt> <dt>

[**Casella di gruppo**](group-box.md)
</dt> <dt>

[**RadioButton**](radio-button.md)
</dt> </dl>

 

 





