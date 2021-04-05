---
title: Pulsante di opzione (riferimento all'elemento MSAA UI)
description: I pulsanti di opzione vengono usati per selezionare una delle diverse opzioni, in genere all'interno di una finestra di dialogo.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9766e85f530281e4f843c4d39fd41fe35d4fb620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708632"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Pulsante di opzione (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti **pulsante di opzione** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **pulsante di opzione** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

I pulsanti di opzione vengono usati per selezionare una delle diverse opzioni, in genere all'interno di una finestra di dialogo. Un pulsante di opzione contiene un piccolo cerchio con testo accanto. Quando questa opzione è selezionata, il cerchio ha un cerchio riempito più piccolo al suo interno. Selezionando un pulsante in un set viene deselezionato il pulsante selezionato in precedenza, quindi solo una delle opzioni del set viene selezionata alla volta.

Il nome della classe della finestra per un pulsante di opzione è "BUTTON".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un pulsante di opzione supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) fa clic sul pulsante di opzione. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un pulsante di opzione supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La proprietà **childCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La proprietà **DefaultAction** per un pulsante di opzione è "check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso del pulsante di opzione, che è un carattere sottolineato nel testo della finestra del controllo. Questa stringa contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** viene ottenuta dal testo o dalla didascalia della finestra del controllo, che viene visualizzata con il pulsante di opzione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha la stessa proprietà **Name** e il nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**\_ \_ RadioButton del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato [**\_ sistema \_ invisibile**](object-state-constants.md) stato sistema stato non \| [**\_ \_ disponibile**](object-state-constants.md) sistema stato stato attivo sistema stato stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ attivo**](object-state-constants.md) sistema stato \| [**\_ \_ selezionato**](object-state-constants.md) \| [**\_ \_ normale**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casella di controllo**](check-box.md)
</dt> <dt>

[**Casella di gruppo**](group-box.md)
</dt> <dt>

[**Pulsante di push**](push-button.md)
</dt> </dl>

 

 





