---
title: Pattern di controllo Styles
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IStylesProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Styles viene usato per descrivere un elemento dell'interfaccia utente con uno stile, un colore di riempimento, un motivo di riempimento o una forma specifici.
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Styles
- Automazione interfaccia utente,Pattern di controllo Stili
- Automazione interfaccia utente,IStylesProvider
- IStylesProvider
- Implementazione del pattern di controllo Automazione interfaccia utente styles
- Pattern di controllo Styles
- pattern di controllo,IStylesProvider
- pattern di controllo, implementazione Automazione interfaccia utente stili
- pattern di controllo,stili
- interfacce,IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e52a6829e592cc659d5ce47b51a09b6d8910d4bd2c41a1e03c9b661d027fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324089"
---
# <a name="styles-control-pattern"></a>Pattern di controllo Styles

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), incluse informazioni su proprietà e metodi. Il **pattern di** controllo Styles viene usato per descrivere un elemento dell'interfaccia utente con uno stile, un colore di riempimento, un motivo di riempimento o una forma specifici.

Il **pattern di** controllo Styles è particolarmente utile per descrivere gli elementi di un documento, che spesso hanno tali stili. Gli stili includono in genere informazioni utili per i clienti con disabilità; Ad esempio, uno stile può descrivere una determinata stringa come titolo di un documento o un determinato oggetto diagramma di flusso come rombo o cerchio. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IStylesProvider**](#required-members-for-istylesprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Styles,** tenere presente le linee guida e le convenzioni seguenti:

-   Il file di intestazione UIAutomationClient.h definisce un set di valori costanti denominati usati per identificare diversi stili comuni. Per altre informazioni, vedere [**Identificatori di stile**](uiauto-style-identifiers.md).
-   Se si usa [**StyleId \_ Custom,**](uiauto-style-identifiers.md)è necessario implementare la proprietà [**IStylesProvider::StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) per consentire ai client di individuare il nome dello stile. Non è necessario implementare la proprietà **StyleName** per uno stile standard perché Microsoft Automazione interfaccia utente fornisce un nome predefinito, ma è possibile implementarlo se è necessario eseguire l'override del nome predefinito.
-   Le altre proprietà nel modello **Styles** sono facoltative. il provider può restituire [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) per una proprietà non supportata.
-   Gli stili in un intervallo di testo possono essere rappresentati tramite gli attributi di testo seguenti:
    -   Quando si risponde a una richiesta per l'attributo di testo [**StyleId,**](uiauto-textattribute-ids.md) l'intervallo di testo deve restituire uno degli identificatori di stile descritti in [**Identificatori di stile**](uiauto-style-identifiers.md).
    -   Se [**si usa StyleId \_ Custom,**](uiauto-style-identifiers.md) l'intervallo di testo deve restituire un valore stringa per l'attributo di testo [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) per consentire ai client di individuare il nome dello stile.
    -   Un intervallo di testo con più stili, ad esempio intestazione e testo normale, deve restituire la speciale proprietà [**reservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) di Automazione interfaccia utente per le proprietà [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) [**e StyleName.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) Un client che riceve questa risposta può suddividere l'intervallo di testo per trovare dove iniziano e terminano gli stili.
-   Le applicazioni possono usare un'ampia gamma di stili per descrivere gli oggetti, Automazione interfaccia utente rappresenta solo quelli più comuni. Per rappresentare attributi di stile aggiuntivi, ad esempio il colore del bordo, un provider può restituire un elenco di attributi aggiuntivi nella [**proprietà ExtendedProperties.**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) Si tratta fondamentalmente di un contenitore di proprietà con un set di proprietà estese, ad esempio "BorderColor=0xFF0000; BorderStyle=dotted". I valori delle proprietà estese possono essere specifici dell'applicazione.

## <a name="required-members-for-istylesprovider"></a>Membri obbligatori per **IStylesProvider**

Per l'implementazione [**dell'interfaccia IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) sono necessarie le proprietà seguenti.



| Membri obbligatori                                                            | Tipo di membro | Note |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | Proprietà    | Nessuno  |
| [**Fillcolor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | Proprietà    | Nessuno  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | Proprietà    | Nessuno  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | Proprietà    | Nessuno  |
| [**Forma**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | Proprietà    | Nessuno  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | Proprietà    | Nessuno  |
| [**Nome stile**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | Proprietà    | Nessuno  |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 