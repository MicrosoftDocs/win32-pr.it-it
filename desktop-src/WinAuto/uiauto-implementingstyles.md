---
title: Pattern di controllo Styles
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IStylesProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Styles viene usato per descrivere un elemento dell'interfaccia utente con uno stile, un colore di riempimento, un modello di riempimento o una forma specifici.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Automazione interfaccia utente, modello di controllo di implementazione degli stili
- Automazione interfaccia utente, pattern di controllo Styles
- Automazione interfaccia utente, IStylesProvider
- IStylesProvider
- implementazione del pattern di controllo stili di automazione interfaccia utente
- Pattern di controllo Styles
- pattern di controllo, IStylesProvider
- pattern di controllo, implementazione di stili di automazione interfaccia utente
- pattern di controllo, stili
- interfacce, IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729602"
---
# <a name="styles-control-pattern"></a>Pattern di controllo Styles

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **Styles** viene usato per descrivere un elemento dell'interfaccia utente con uno stile, un colore di riempimento, un modello di riempimento o una forma specifici.

Il pattern di controllo **Styles** è particolarmente utile per descrivere gli elementi di un documento, che hanno spesso tali stili. Gli stili contengono in genere informazioni utili per i clienti con disabilità; uno stile, ad esempio, può descrivere una determinata stringa come titolo di un documento o un determinato oggetto diagramma di flusso come un rombo o un cerchio. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IStylesProvider**](#required-members-for-istylesprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Styles** , tenere presenti le linee guida e le convenzioni seguenti:

-   Il file di intestazione UIAutomationClient. h definisce un set di valori costanti denominati usati per identificare diversi stili comuni. Per altre informazioni, vedere [**identificatori di stile**](uiauto-style-identifiers.md).
-   Se si usa [**StyleId \_ personalizzato**](uiauto-style-identifiers.md), è necessario implementare la proprietà [**IStylesProvider:: styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) per consentire ai client di individuare il nome dello stile. Non è necessario implementare la proprietà **styleName** per uno stile standard perché automazione interfaccia utente Microsoft fornisce un nome predefinito, ma è possibile implementarlo se è necessario eseguire l'override del nome predefinito.
-   Le altre proprietà nel modello di **stili** sono facoltative; il provider può restituire l'interfaccia [**\_ \_ NotSupported E**](uiauto-error-codes.md) la proprietà non supportata.
-   Gli stili in un intervallo di testo possono essere rappresentati tramite gli attributi di testo seguenti:
    -   Quando si risponde a una richiesta per l'attributo di testo [**StyleId**](uiauto-textattribute-ids.md) , l'intervallo di testo deve restituire uno degli identificatori di stile descritti in [**identificatori di stile**](uiauto-style-identifiers.md).
    -   Se si usa [**StyleId \_ Custom**](uiauto-style-identifiers.md) , l'intervallo di testo deve restituire un valore stringa per l'attributo di testo [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) per consentire ai client di individuare il nome dello stile.
    -   Un intervallo di testo con più stili, ad esempio l'intestazione e il testo normale, deve restituire la speciale proprietà [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) di automazione interfaccia utente per entrambe le proprietà [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) e [**styleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) . Un client che riceve questa risposta può suddividere l'intervallo di testo per individuare il punto in cui iniziano e terminano gli stili.
-   Le applicazioni possono usare un'ampia gamma di stili per descrivere gli oggetti, ma l'automazione dell'interfaccia utente rappresenta solo le più comuni. Per rappresentare altri attributi di stile, ad esempio il colore del bordo, un provider può restituire un elenco di attributi aggiuntivi nella proprietà [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) . Si tratta fondamentalmente di un elenco di proprietà con un set di proprietà estese, ad esempio "BorderColor = 0xFF0000; BorderStyle = punteggiato ". I valori delle proprietà estese possono essere specifici dell'applicazione.

## <a name="required-members-for-istylesprovider"></a>Membri obbligatori per **IStylesProvider**

Le proprietà seguenti sono necessarie per l'implementazione dell'interfaccia [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) .



| Membri obbligatori                                                            | Tipo di membro | Note |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Proprietà    | nessuno  |
| [**FillColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Proprietà    | nessuno  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Proprietà    | nessuno  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Proprietà    | nessuno  |
| [**Con forme**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Proprietà    | nessuno  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Proprietà    | nessuno  |
| [**Nome stile**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Proprietà    | nessuno  |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 