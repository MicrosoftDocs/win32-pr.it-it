---
title: Pattern di controllo SpreadsheetItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISpreadsheetItemProvider, incluse informazioni su proprietà e metodi.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo SpreadsheetItem
- Automazione interfaccia utente,Pattern di controllo SpreadsheetItem
- Automazione interfaccia utente,ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- Implementazione di Automazione interfaccia utente di controllo SpreadsheetItem
- Pattern di controllo SpreadsheetItem
- pattern di controllo,ISpreadsheetItemProvider
- pattern di controllo, implementazione Automazione interfaccia utente SpreadsheetItem
- pattern di controllo,SpreadsheetItem
- interfacce,ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d5feaa32b5fe79635c6acc01e1e0b18b9ba77c382ba3f07c64f7cb3e921b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324371"
---
# <a name="spreadsheetitem-control-pattern"></a>Pattern di controllo SpreadsheetItem

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di ISpreadsheetItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)incluse informazioni su proprietà e metodi. Il **pattern di controllo SpreadsheetItem** viene usato per esporre le proprietà di una cella in un foglio di calcolo o in un altro documento basato su griglia.

Il **pattern di controllo SpreadsheetItem** è strettamente correlato al pattern di controllo [GridItem.](uiauto-implementinggriditem.md) Anche i controlli che implementano il pattern di **controllo SpreadsheetItem** devono implementare il pattern di controllo GridItem. I controlli possono anche implementare il pattern [di controllo TableItem,](uiauto-implementingtableitem.md) se appropriato. Per esempi di controlli che implementano questi pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo SpreadsheetItem,** tenere presente le linee guida e le convenzioni seguenti:

-   Quando si implementano i metodi [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) e [**ISpreadsheetItemProvider::GetAnnotationTypes,**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) vedere la documentazione [**di IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Entrambi i metodi restituiscono matrici per consentire ai provider di supportare più annotazioni in una singola cella.
-   Alcuni tipi di annotazioni non richiedono un'implementazione completa [**dell'interfaccia IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Ad esempio, un semplice indicatore di errore di ortografia può essere rappresentato facendo in modo che [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) restituirà un identificatore di attributo di testo [**annotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e che [**GetAnnotationObjects restituirà**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) un valore Null.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Membri obbligatori per **ISpreadsheetItemProvider**

Le proprietà e i metodi seguenti sono necessari per l'implementazione [**dell'interfaccia ISpreadsheetItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)



| Membri obbligatori                                                                         | Tipo di membro | Note                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Proprietà    | L'implementazione [**di una proprietà Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) separata è necessaria perché la proprietà [Value](value-property.md) di una cella restituisce in genere il valore calcolato della cella. La **proprietà Formula** deve essere NULL **se** non è impostata alcuna formula. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Metodo      | Restituisce una matrice di provider di elementi che fanno riferimento alle annotazioni collegate a questa cella. I puntatori all'interno della matrice possono essere Null se un'annotazione non ha un provider collegato.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Metodo      | Restituisce una matrice di identificatori del tipo di annotazione che descrivono le annotazioni in questa cella. La matrice deve avere le stesse dimensioni della matrice restituita da [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).                                         |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo foglio di calcolo](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 