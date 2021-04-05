---
title: Informazioni sul modello a oggetti testo di automazione interfaccia utente
description: Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft accedono al contenuto testuale di un controllo basato su testo.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- client, informazioni sul modello a oggetti testo di automazione interfaccia utente
- client, controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo Text
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709340"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Informazioni sul modello a oggetti testo di automazione interfaccia utente

Questo argomento descrive il modo in cui le applicazioni client di automazione interfaccia utente Microsoft accedono al contenuto testuale di un controllo basato su testo.

-   [Modello a oggetti specifico del controllo](#control-specific-object-model)
-   [Argomenti correlati](#related-topics)

I controlli basati su testo espongono contenuto testuale per le applicazioni client di automazione interfaccia utente tramite un modello a oggetti testo semplice. Le applicazioni client possono accedere al modello a oggetti testo tramite le interfacce del pattern [di controllo Text e TextRange](uiauto-about-text-and-textrange-patterns.md) , inclusi [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Le applicazioni client possono usare queste interfacce per recuperare contenuto testuale, attributi di testo e oggetti incorporati, ad esempio tabelle e collegamenti ipertestuali, da controlli basati su testo.

I tipi di controllo che supportano il modello a oggetti testo di automazione interfaccia utente includono i tipi di controllo [modifica](uiauto-supporteditcontroltype.md) e [documento](uiauto-supportdocumentcontroltype.md) . Altri tipi di controllo, ad esempio [Descrizione comando](uiauto-supporttooltipcontroltype.md) e [testo](uiauto-supporttextcontroltype.md) , potrebbero supportare anche il modello a oggetti testo, ma non sono obbligatori.

> [!Note]  
> Il modello a oggetti testo di automazione interfaccia utente non fornisce un mezzo per inserire o modificare il testo. Tuttavia, alcuni controlli consentono di inserire o modificare il testo tramite l'interfaccia [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) o tramite input diretto da tastiera.

 

## <a name="control-specific-object-model"></a>Modello a oggetti specifico del controllo

Un controllo basato su testo che implementa il proprio Document Object Model (DOM) può esporre il DOM implementando il pattern di controllo [ObjectModel](uiauto-implementingobjectmodel.md) . L'esposizione del DOM può consentire alle applicazioni client di accedere e controllare ulteriormente il contenuto di un controllo basato su testo.

Un'applicazione client può individuare se un particolare controllo basato su testo implementa un DOM recuperando l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del controllo. Chiamare quindi il metodo [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , specificando l'identificatore della proprietà [**\_ IsObjectModelPatternAvailablePropertyId di UIA**](uiauto-control-pattern-availability-propids.md) e una variante che riceve true se il controllo implementa un Dom.

Per accedere al DOM, chiamare il metodo [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , specificando l'identificatore del pattern di controllo [**\_ ObjectModelPatternId di UIA**](uiauto-controlpattern-ids.md) e una variabile che riceve l'interfaccia [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) . Chiamare il metodo [**IUIAutomationObjectModelPattern:: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) per recuperare l'interfaccia Dom.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilizzo di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




