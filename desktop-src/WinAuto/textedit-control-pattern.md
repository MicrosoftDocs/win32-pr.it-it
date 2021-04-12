---
title: Pattern di controllo TextEdit
description: Introduce le linee guida e le convenzioni per l'implementazione di ITextEditProvider, incluse informazioni su proprietà e metodi.
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo TextEdit
- Automazione interfaccia utente, pattern di controllo TextEdit
- pattern di controllo, TextEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339094"
---
# <a name="textedit-control-pattern"></a>Pattern di controllo TextEdit

Introduce le linee guida e le convenzioni per l'implementazione di [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **TextEdit** viene usato per l'accesso a livello di codice a un controllo che modifica il testo, ad esempio un controllo che esegue la correzione automatica o Abilita la composizione di input.

> [!Note]  
> Le note di implementazione in questo argomento fanno riferimento alle API che provengono da Text Services Framework (TSF). Per altre informazioni su TSF e sui riferimenti alle API, vedere [Text Services Framework](/windows/desktop/TSF/text-services-framework).

 

## <a name="required-members-for-itexteditprovider"></a>Membri obbligatori per **ITextEditProvider**

Queste proprietà e questi metodi sono necessari per implementare l'interfaccia [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) .



| Membri obbligatori                                                              | Tipo di membro | Note                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetActiveComposition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | Metodo      | Restituisce l'intervallo della conversione corrente (nessuno se non esiste alcuna conversione). Restituisce la composizione attiva (in TSF, questo è l'intervallo contrassegnato dalla **\_ \_ composizione della prop GUID**). Ad esempio, con Microsoft Japanese input Method Editor (IME), si tratta del testo sottolineato completo. |
| [**GetConversionTarget**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | Metodo      | Restituisce l'intervallo di destinazione della conversione corrente (nessuno se nessuna conversione). In TSF, questo è l'intervallo di caratteri contrassegnati come **tf \_ attr \_ target \_ NOTCONVERTED** o **tf \_ attr \_ target \_ convertito** dalla struttura **tf \_ DISPLAYATTRIBUTE** .                                               |



 

Gli eventi **TextEditTextChanged** e **ConversionTargetChanged** devono essere generati dagli elementi di automazione interfaccia utente Microsoft che supportano il modello **TextEdit** .

### <a name="textedittextchanged"></a>**TextEditTextChanged**

-   Utilizzare la funzione [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) per generare l'evento **TextEditTextChanged** .
-   La tabella seguente elenca i casi in cui è necessario generare l'evento e i parametri [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) da usare.



| TextEditChangeType                                            | Payload dell'evento                                | Note                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Correzione automatica**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Nuova stringa con correzione                         | Generato quando viene apportata una correzione automatica dal controllo. O ogni volta che viene eseguita una sostituzione tramite TSF e l'intervallo ha un **GUID \_ prop \_ TKB \_ alternations** valore di **TKB \_ alterna la \_ correzione automatica \_ applicata**.<br/>                                                                                                                                                                   |
| [**Composizione**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | Stringa aggiornata                           | Il payload deve includere solo i caratteri modificati (non inviare l'intera stringa di composizione). Generato ogni volta che viene eseguita una sostituzione della composizione. In TSF, una sostituzione di composizione viene definita come sostituzione con il flag di composizione **GUID \_ prop \_** impostato. I controlli di modifica che implementano TSF possono monitorare queste modifiche tramite la notifica **OnEndEdit** .<br/>         |
| [**CompositionFinalized**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | Stringa di composizione finalizzata (vedere le note) | In TSF la stringa di conversione da finalizzare è definita dal flag **di \_ \_ composizione del GUID** che viene rimosso da una composizione. I controlli di modifica che implementano TSF devono determinare la stringa finalizzata da **EndComposition** e generare l'evento quando viene chiamato **OnEndEdit** .<br/> La stringa di composizione finalizzata può essere vuota se la composizione è stata annullata o eliminata.<br/> |



 

### <a name="conversiontargetchanged"></a>**ConversionTargetChanged**

-   **ConversionTargetChanged** si verifica quando la destinazione della conversione viene modificata da una destinazione a un'altra.
-   Usare la funzione [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) per generare l'evento **ConversionTargetChanged** (passare l'identificatore dell'evento [**ConversionTargetChangedEventId per UIA \_ TextEdit \_**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) ).
-   **ConversionTargetChanged** non deve essere generato quando viene modificato il contenuto della destinazione. Se la modifica di destinazione si verifica simultaneamente con una modifica della composizione, l'evento di modifica di destinazione deve essere generato dopo che sono già stati generati eventi di composizione.
-   In TSF la destinazione della conversione viene definita dal valore di **\_ destinazione TF \_ attr \_ convertito** da impostato dalla struttura **tf \_ DISPLAYATTRIBUTE** . È possibile monitorare le modifiche utilizzando **OnEndEdit**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

