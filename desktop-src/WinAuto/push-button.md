---
title: Pulsante di push (riferimento all'elemento MSAA UI)
description: Un pulsante di push è un piccolo oggetto rettangolare usato per eseguire un'azione. Ad esempio, i pulsanti OK e Annulla in una finestra di dialogo sono pulsanti di push.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e188b58501509fd934ab6396a21beb209857661
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709955"
---
# <a name="push-button-msaa-ui-element-reference"></a>Pulsante di push (riferimento all'elemento MSAA UI)

Un pulsante di push è un piccolo oggetto rettangolare usato per eseguire un'azione. Ad esempio, i pulsanti **OK** e **Annulla** in una finestra di dialogo sono pulsanti di push.

Il nome della classe della finestra per un pulsante di push è "BUTTON".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un pulsante di push supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) fa clic sul pulsante di push. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un pulsante di push supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è zero o più.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La proprietà **DefaultAction** è "premere".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso del pulsante, che è un carattere sottolineato nel testo del testo della finestra del pulsante. Ad esempio, "Alt + o" è la proprietà **KeyboardShortcut** per un pulsante **OK** .                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** viene ottenuta dal testo o dalla didascalia della finestra del controllo, che viene visualizzata nel pulsante di push. Ad esempio, "OK" è la proprietà **Name** per un pulsante **OK** .                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**il \_ \_ pulsante del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei seguenti [valori](object-state-constants.md): stato [**\_ sistema \_ invisibile**](object-state-constants.md) allo stato sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) sistema stato \| [**\_ \_ attivato**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casella di controllo**](check-box.md)
</dt> <dt>

[**Casella di gruppo**](group-box.md)
</dt> <dt>

[**RadioButton**](radio-button.md)
</dt> </dl>

 

 





