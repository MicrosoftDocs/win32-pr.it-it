---
title: Informazioni sul modello Automazione interfaccia utente a oggetti di testo
description: Questo argomento descrive come Microsoft Automazione interfaccia utente applicazioni client accedono al contenuto testuale di un controllo basato su testo.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- client, comprensione del Automazione interfaccia utente a oggetti di testo
- client, controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo del testo
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655f291e9cc11d925f947617fe31be96ebd81a2dbff73506a0e474dcde9e4446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823893"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Informazioni sul modello Automazione interfaccia utente a oggetti di testo

Questo argomento descrive come Microsoft Automazione interfaccia utente applicazioni client accedono al contenuto testuale di un controllo basato su testo.

-   [Modello a oggetti specifico del controllo](#control-specific-object-model)
-   [Argomenti correlati](#related-topics)

I controlli basati su testo espongono contenuto testuale Automazione interfaccia utente applicazioni client tramite un semplice modello a oggetti di testo. Le applicazioni client hanno accesso al modello a oggetti di testo tramite le interfacce del pattern di controllo Text e [TextRange,](uiauto-about-text-and-textrange-patterns.md) tra cui [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) Le applicazioni client possono usare queste interfacce per recuperare contenuto testuale, attributi di testo e oggetti incorporati, ad esempio tabelle e collegamenti ipertestuali da controlli basati su testo.

I tipi di controllo che supportano il Automazione interfaccia utente a oggetti di testo includono [i tipi di](uiauto-supporteditcontroltype.md) controllo Modifica e Documento. [](uiauto-supportdocumentcontroltype.md) Anche altri tipi di controllo, ad esempio [Descrizione](uiauto-supporttooltipcontroltype.md) comando e [Testo,](uiauto-supporttextcontroltype.md) possono supportare il modello a oggetti di testo, ma non è necessario.

> [!Note]  
> Il Automazione interfaccia utente a oggetti di testo non fornisce un mezzo per inserire o modificare il testo. Tuttavia, alcuni controlli consentono l'inserimento o la modifica del testo tramite [**l'interfaccia IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) o tramite input diretto da tastiera.

 

## <a name="control-specific-object-model"></a>Modello a oggetti specifico del controllo

Un controllo basato su testo che implementa il proprio Document Object Model (DOM) può esporre il DOM implementando il pattern [di controllo ObjectModel.](uiauto-implementingobjectmodel.md) L'esposizione del DOM può offrire alle applicazioni client maggiore accesso e controllo sul contenuto di un controllo basato su testo.

Un'applicazione client può individuare se un determinato controllo basato su testo implementa un DOM recuperando [**l'interfaccia IUIAutomationElement del**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) controllo. Chiamare quindi il metodo [**IUIAutomationElement::GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) specificando l'identificatore della proprietà [**\_ UiA IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) e una variante che riceve TRUE se il controllo implementa un DOM.

Per accedere al DOM, chiamare il metodo [**IUIAutomationElement::GetCurrentPattern,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) specificando l'identificatore del pattern di controllo [**\_ UIA ObjectModelPatternId**](uiauto-controlpattern-ids.md) e una variabile che riceve l'interfaccia [**IUIAutomationObjectModelPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) Chiamare il [**metodo IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) per recuperare l'interfaccia DOM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




