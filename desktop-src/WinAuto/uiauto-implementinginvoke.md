---
title: Pattern di controllo Invoke
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IInvokeProvider, incluse informazioni sui metodi.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Invoke
- Automazione interfaccia utente, pattern di controllo Invoke
- Automazione interfaccia utente, IInvokeProvider
- IInvokeProvider
- implementazione di pattern di controllo Invoke di automazione interfaccia utente
- Richiama pattern di controllo
- pattern di controllo, IInvokeProvider
- pattern di controllo, implementazione di Invoke di automazione interfaccia utente
- pattern di controllo, Invoke
- interfacce, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855922"
---
# <a name="invoke-control-pattern"></a>Pattern di controllo Invoke

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), incluse informazioni sui metodi. Il pattern di controllo **Invoke** viene usato per supportare i controlli che non mantengono lo stato quando sono attivati, bensì avviano o eseguono una singola azione non ambigua.

I controlli che mantengono lo stato, ad esempio caselle di controllo e pulsanti di opzione, devono invece implementare rispettivamente [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) e [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) . Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Invoke** , tenere presenti le linee guida e le convenzioni seguenti:

-   I controlli implementano [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) se lo stesso comportamento non viene esposto tramite un altro provider di pattern di controllo. Se, ad esempio, il metodo [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) su un controllo esegue la stessa azione del metodo [**IUIAutomationExpandCollapsePattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) o [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , il controllo non deve implementare **IInvokeProvider**.
-   La chiamata di un controllo viene in genere eseguita facendo clic o doppio clic oppure premendo INVIO, una scelta rapida predefinita da tastiera o una combinazione alternativa di tasti.
-   L'evento **richiamato** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) viene generato su un controllo che è stato attivato (come risposta a un controllo che esegue l'azione associata). Se possibile, l'evento deve essere generato dopo che il controllo ha completato l'azione ed è stato restituito senza alcun blocco. L'evento **richiamato** (**UIA \_ Invoke \_ InvokedEventId**) deve essere generato prima della manutenzione della richiesta **Invoke** negli scenari seguenti:
    -   Non è possibile o conveniente attendere il completamento dell'azione.
    -   L'azione richiede l'intervento dell'utente.
    -   L'azione è dispendiosa a livello di tempo e comporta il blocco del client chiamante un periodo di tempo significativo.
-   Se il richiamo del controllo è caratterizzato da effetti collaterali significativi, tali effetti collaterali devono essere esposti tramite la proprietà **HelpText** . Ad esempio, anche se [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) non è associato alla selezione, **Invoke** può causare la selezione di un altro controllo.
-   Gli effetti del passaggio del mouse (o del mouse su) in genere non costituiscono un evento **richiamato** . Tuttavia, i controlli che eseguono un'azione, anziché causare un effetto visivo, basati sullo stato del passaggio del mouse devono supportare il pattern di controllo **Invoke** .
    > [!Note]  
    > Questa implementazione viene considerata un problema di accessibilità se il controllo può essere chiamato solo come risultato di un effetto collaterale relativo al mouse.

     

-   La chiamata di un controllo è diversa dalla selezione di un elemento. Tuttavia, a seconda del controllo, come effetto collaterale la chiamata potrebbe causare la selezione dell'elemento. Ad esempio, la chiamata di un elemento dell'elenco di documenti di Microsoft Word nella cartella documenti seleziona l'elemento e apre il documento.
-   Un elemento può scomparire dall'albero di automazione interfaccia utente Microsoft immediatamente dopo essere stato richiamato. Di conseguenza, la richiesta di informazioni dall'elemento fornito dal callback di evento potrebbe avere esito negativo. La prelettura delle informazioni memorizzate nella cache rappresenta la soluzione alternativa consigliata.
-   I controlli possono implementare più pattern di controllo. Ad esempio, il controllo **colore riempimento** sulla barra degli strumenti di Microsoft Excel implementa sia il pattern di controllo Invoke che il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) . Il pattern di controllo ExpandCollapse espone il menu e il pattern di controllo **Invoke** riempie la selezione attiva con il colore scelto.

## <a name="required-members-for-iinvokeprovider"></a>Membri obbligatori per **IInvokeProvider**

Il metodo seguente è necessario per implementare l'interfaccia [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .



| Membri obbligatori                                | Tipo di membro | Note                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Richiamare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Metodo      | **Invoke** è una chiamata asincrona e deve restituire immediatamente un valore senza blocco.<br/> Questo comportamento è particolarmente critico per i controlli che direttamente o indirettamente avviano una finestra di dialogo quando vengono chiamati. Qualsiasi client di automazione interfaccia utente che ha generato l'evento rimarrà bloccato fino a quando non viene chiusa la finestra di dialogo modale. <br/> |



 

Questo pattern di controllo non è associato a proprietà o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)
</dt> </dl>

 

 





