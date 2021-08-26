---
title: Pulsante di opzione (riferimento all'elemento DELL'interfaccia utente MSAA)
description: I pulsanti di opzione vengono usati per selezionare una delle diverse opzioni, in genere all'interno di una finestra di dialogo.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c560e4efa57790980d852ab2716248d5b1d7faff535592f3f2ca892f3dff0715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998141"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Pulsante di opzione (riferimento all'elemento DELL'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Pulsante di opzione** ai fini del riferimento agli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Pulsante di** opzione in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

I pulsanti di opzione vengono usati per selezionare una delle diverse opzioni, in genere all'interno di una finestra di dialogo. Un pulsante di opzione contiene un piccolo cerchio con il testo accanto. Quando è selezionato, il cerchio ha un cerchio più piccolo e pieno al suo interno. Se si seleziona un pulsante in un set, il pulsante selezionato in precedenza viene deselezionato, quindi viene selezionata solo una delle opzioni del set alla volta.

Il nome della classe della finestra per un pulsante di opzione è "BUTTON".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un pulsante di opzione supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Metodo                                                                    | Commenti                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Il [**metodo accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) fa clic sul pulsante di opzione. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un pulsante di opzione supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **proprietà DefaultAction** per un pulsante di opzione è "Check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta del pulsante di opzione, ovvero un carattere sottolineato nel testo della finestra del controllo. Questa stringa contiene il carattere del tasto di scelta aggiunto alla stringa "ALT+".                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** viene ottenuta dal testo (o didascalia) della finestra del controllo, visualizzato con il pulsante di opzione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ RADIOBUTTON.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ CHECKED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ NORMAL**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casella di controllo**](check-box.md)
</dt> <dt>

[**Casella di gruppo**](group-box.md)
</dt> <dt>

[**Pulsante**](push-button.md)
</dt> </dl>

 

 





