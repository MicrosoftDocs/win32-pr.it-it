---
title: Pattern di controllo Invoke
description: Descrive le linee guida e le convenzioni per l'implementazione di IInvokeProvider, incluse le informazioni sui metodi.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Invoke
- Automazione interfaccia utente,Invoke control pattern
- Automazione interfaccia utente,IInvokeProvider
- IInvokeProvider
- implementazione di Automazione interfaccia utente invoke
- Richiamare pattern di controllo
- pattern di controllo, IInvokeProvider
- pattern di controllo, implementazione Automazione interfaccia utente Invoke
- pattern di controllo, invoke
- interfacce, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbd675a9c30daf0e7b097a706dae9ff0d7767f92f7b785b3098d72ddf6f7cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997941"
---
# <a name="invoke-control-pattern"></a>Pattern di controllo Invoke

Descrive le linee guida e le convenzioni per l'implementazione [**di IInvokeProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)incluse le informazioni sui metodi. Il pattern di controllo **Invoke** viene usato per supportare i controlli che non mantengono lo stato quando vengono attivati, ma avviano o eseguono una singola azione non ambigua.

I controlli che mantengono lo stato, ad esempio caselle di controllo e pulsanti di opzione, devono invece implementare [**rispettivamente IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) [**e ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Invoke,** tenere presente le linee guida e le convenzioni seguenti:

-   I controlli [**implementano IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) se lo stesso comportamento non viene esposto tramite un altro provider del pattern di controllo. Ad esempio, se il metodo [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) su un controllo esegue la stessa azione del metodo [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) o [**Collapse,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) il controllo non deve implementare **IInvokeProvider**.
-   La chiamata di un controllo viene in genere eseguita facendo clic o doppio clic oppure premendo INVIO, una scelta rapida predefinita da tastiera o una combinazione alternativa di tasti.
-   **L'evento Invoked** ([**UIA \_ \_ InvokedEventId**](uiauto-event-ids.md)) viene generato su un controllo attivato (in risposta a un controllo che effettua l'azione associata). Se possibile, l'evento deve essere generato dopo che il controllo ha completato l'azione ed è stato restituito senza alcun blocco. **L'evento Invoked** (**UIA \_ \_ InvokedEventId**) deve essere generato prima di eseguire la richiesta **Invoke** negli scenari seguenti:
    -   Non è possibile o conveniente attendere il completamento dell'azione.
    -   L'azione richiede l'intervento dell'utente.
    -   L'azione è dispendiosa a livello di tempo e comporta il blocco del client chiamante un periodo di tempo significativo.
-   Se la chiamata del controllo ha effetti collaterali significativi, tali effetti collaterali devono essere esposti tramite la **proprietà HelpText.** Ad esempio, anche se [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) non è associato alla selezione, **Invoke** può causare la selezione di un altro controllo.
-   Gli effetti di passaggio del mouse (o passaggio del mouse) in genere non costituiscono un **evento Richiamato.** Tuttavia, i controlli che eseguono un'azione (anziché causare un effetto visivo) in base allo stato del passaggio del mouse devono supportare il pattern di controllo **Invoke.**
    > [!Note]  
    > Questa implementazione viene considerata un problema di accessibilità se il controllo può essere chiamato solo come risultato di un effetto collaterale relativo al mouse.

     

-   La chiamata di un controllo è diversa dalla selezione di un elemento. Tuttavia, a seconda del controllo, come effetto collaterale la chiamata potrebbe causare la selezione dell'elemento. Ad esempio, richiamando un Microsoft Word di elenco di documenti nella cartella Documenti, l'elemento viene selezionato e aperto.
-   Un elemento può scomparire dall'albero Automazione interfaccia utente Microsoft immediatamente dopo essere stato richiamato. Di conseguenza, la richiesta di informazioni dall'elemento fornito dal callback di evento potrebbe avere esito negativo. La prelettura delle informazioni memorizzate nella cache rappresenta la soluzione alternativa consigliata.
-   I controlli possono implementare più pattern di controllo. Ad esempio, il **controllo Colore di** riempimento sulla barra Microsoft Excel barra degli strumenti implementa entrambi i pattern di controllo Invoke e [ExpandCollapse.](uiauto-implementingexpandcollapse.md) Il pattern di controllo ExpandCollapse espone il menu e il pattern di controllo **Invoke** riempie la selezione attiva con il colore scelto.

## <a name="required-members-for-iinvokeprovider"></a>Membri obbligatori per **IInvokeProvider**

Il metodo seguente è necessario per l'implementazione [**dell'interfaccia IInvokeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)



| Membri obbligatori                                | Tipo di membro | Note                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**evocare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Metodo      | **Invoke** è una chiamata asincrona e deve essere restituito immediatamente senza blocco.<br/> Questo comportamento è particolarmente critico per i controlli che direttamente o indirettamente avviano una finestra di dialogo quando vengono chiamati. Qualsiasi client di automazione interfaccia utente che ha generato l'evento rimarrà bloccato fino a quando non viene chiusa la finestra di dialogo modale. <br/> |



 

Questo pattern di controllo non è associato a proprietà o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[**\_ \_ InvokedEventId dell'interfaccia utente**](uiauto-event-ids.md)
</dt> </dl>

 

 





