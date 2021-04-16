---
title: Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente
description: I tipi di controllo di automazione interfaccia utente Microsoft sono proprietà che vengono utilizzate come identificatori noti che indicano il tipo di controllo rappresentato da un particolare elemento dell'interfaccia utente, ad esempio una casella combinata o un pulsante.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Automazione interfaccia utente, panoramica sui tipi di controllo
- Automazione interfaccia utente, proprietà UIA_LocalizedControlTypePropertyId
- tipi di controllo, informazioni
- tipi di controllo, requisiti
- tipi di controllo, prerequisiti
- tipi di controllo, predefiniti
- tipi di controllo, proprietà UIA_LocalizedControlTypePropertyId
- tipi di controllo predefiniti
- Proprietà UIA_LocalizedControlTypePropertyId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516822"
---
# <a name="ui-automation-control-types-overview"></a>Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente

I tipi di controllo di automazione interfaccia utente Microsoft sono proprietà che vengono utilizzate come identificatori noti che indicano il tipo di controllo rappresentato da un particolare elemento dell'interfaccia utente, ad esempio una casella combinata o un pulsante. Le applicazioni client usano il tipo per identificare le funzionalità di un controllo e per determinare come interagire con esso.

In questo argomento sono incluse le sezioni seguenti:

-   [Requisiti per i tipi di controllo per l'automazione dell'interfaccia utente](#ui-automation-control-type-requisites)
-   [Proprietà LocalizedControlType](#the-localizedcontroltype-property)
-   [Tipi di controllo correnti per l'automazione dell'interfaccia utente](#current-ui-automation-control-types)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Requisiti per i tipi di controllo per l'automazione dell'interfaccia utente

A ogni tipo di controllo di automazione interfaccia utente è associato un set di condizioni. Quando un provider assegna un tipo di controllo a un controllo, il provider deve garantire che il controllo soddisfi tutte le condizioni associate a tale tipo di controllo. Di seguito sono riportate le condizioni:

-   Pattern di controllo di automazione interfaccia utente: ogni tipo di controllo ha un set di pattern di controllo che il controllo deve supportare, un set facoltativo e un set che il controllo non deve supportare.
-   Valori di proprietà di automazione interfaccia utente: ogni tipo di controllo ha un set di proprietà che il controllo deve supportare.
-   Eventi di automazione interfaccia utente: ogni tipo di controllo ha un set di eventi che il controllo deve supportare.
-   Struttura dell'albero di automazione interfaccia utente: ogni tipo di controllo stabilisce il modo in cui il controllo deve apparire nella struttura dell'albero di automazione interfaccia utente.

Quando un controllo soddisfa le condizioni per un particolare tipo di controllo, il valore della proprietà [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**IUIAutomationElement:: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indicherà tale tipo di controllo.

Se il controllo non soddisfa le specifiche per un particolare tipo di controllo, usare [**\_ CustomControlTypeId**](uiauto-controltype-ids.md) di gestione dell'interfaccia utente come ID del tipo di controllo e descrivere completamente il controllo usando le proprietà e i pattern di controllo pertinenti. È anche possibile impostare la [**proprietà \_ LocalizedControlTypePropertyId di UIA**](uiauto-automation-element-propids.md) su una stringa che meglio descrive il tipo del controllo.

## <a name="the-localizedcontroltype-property"></a>Proprietà LocalizedControlType

Se si usa un tipo di controllo predefinito per descrivere il controllo, usare il valore predefinito per la [**proprietà \_ LocalizedControlTypePropertyId di UIA**](uiauto-automation-element-propids.md) e consentire all'automazione dell'interfaccia utente di fornire una stringa localizzata per esporre correttamente i provider. Se non è possibile usare un tipo di controllo predefinito per descrivere il controllo, impostare la proprietà **\_ LocalizedControlTypePropertyId di UIA** su una stringa localizzata che descrive in modo accurato il tipo del controllo. La stringa deve essere concisa, ma con una precisione sufficiente che una tecnologia per l'accessibilità, ad esempio un'utilità per la lettura dello schermo, possa utilizzarla nell'interfaccia utente per informare l'utente del tipo del controllo.

## <a name="current-ui-automation-control-types"></a>Tipi di controllo correnti per l'automazione dell'interfaccia utente

Negli argomenti seguenti vengono descritti i tipi di controllo di automazione interfaccia utente. Per ogni tipo di controllo, la descrizione include il set di condizioni che un controllo del tipo specificato deve supportare:

-   Tipo di controllo AppBar
-   [Tipo di controllo Button](uiauto-supportbuttoncontroltype.md)
-   [Tipo di controllo Calendar](uiauto-supportcalendarcontroltype.md)
-   [Tipo di controllo CheckBox](uiauto-supportcheckboxcontroltype.md)
-   [Tipo di controllo ComboBox](uiauto-supportcomboboxcontroltype.md)
-   [Tipo di controllo DataGrid](uiauto-supportdatagridcontroltype.md)
-   [Tipo di controllo DataItem](uiauto-supportdataitemcontroltype.md)
-   [Tipo di controllo Document](uiauto-supportdocumentcontroltype.md)
-   [Modificare il tipo di controllo](uiauto-supporteditcontroltype.md)
-   [Tipo di controllo gruppo](uiauto-supportgroupcontroltype.md)
-   [Tipo di controllo Header](uiauto-supportheadercontroltype.md)
-   [Tipo di controllo HeaderItem](uiauto-supportheaderitemcontroltype.md)
-   [Tipo di controllo HyperLink](uiauto-supporthyperlinkcontroltype.md)
-   [Tipo di controllo Image](uiauto-supportimagecontroltype.md)
-   [Tipo di controllo List](uiauto-supportlistcontroltype.md)
-   [Tipo di controllo ListItem](uiauto-supportlistitemcontroltype.md)
-   [Tipo di controllo menu](uiauto-supportmenucontroltype.md)
-   [Tipo di controllo barra dei menu](uiauto-supportmenubarcontroltype.md)
-   [Tipo di controllo MenuItem](uiauto-supportmenuitemcontroltype.md)
-   [Tipo di controllo pane](uiauto-supportpanecontroltype.md)
-   [Tipo di controllo ProgressBar](uiauto-supportprogressbarcontroltype.md)
-   [RadioButton (tipo di controllo)](uiauto-supportradiobuttoncontroltype.md)
-   [Tipo di controllo ScrollBar](uiauto-supportscrollbarcontroltype.md)
-   [Tipo di controllo SemanticZoom](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Tipo di controllo Separator](uiauto-supportseparatorcontroltype.md)
-   [Tipo di controllo Slider](uiauto-supportslidercontroltype.md)
-   [Tipo di controllo Spinner](uiauto-supportspinnercontroltype.md)
-   [Tipo di controllo SplitButton](uiauto-supportsplitbuttoncontroltype.md)
-   [Tipo di controllo StatusBar](uiauto-supportstatusbarcontroltype.md)
-   [Tipo di controllo Tab](uiauto-supporttabcontroltype.md)
-   [Tipo di controllo TabItem](uiauto-supporttabitemcontroltype.md)
-   [Tipo di controllo Table](uiauto-supporttablecontroltype.md)
-   [Tipo di controllo Text](uiauto-supporttextcontroltype.md)
-   [Tipo di controllo Thumb](uiauto-supportthumbcontroltype.md)
-   [Tipo di controllo barra di titolo](uiauto-supporttitlebarcontroltype.md)
-   [Tipo di controllo ToolBar](uiauto-supporttoolbarcontroltype.md)
-   [Tipo di controllo ToolTip](uiauto-supporttooltipcontroltype.md)
-   [Tipo di controllo Tree](uiauto-supporttreecontroltype.md)
-   [Tipo di controllo TreeItem](uiauto-supporttreeitemcontroltype.md)
-   [Tipo di controllo Window](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Identificatori del tipo di controllo](uiauto-controltype-ids.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Supporto di tipi di controllo di automazione interfaccia utente](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Supporto per automazione interfaccia utente dei controlli standard](uiauto-controlsupport.md)
</dt> <dt>

[Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
</dt> </dl>

 

 