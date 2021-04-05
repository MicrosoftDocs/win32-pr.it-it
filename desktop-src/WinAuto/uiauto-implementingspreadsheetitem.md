---
title: Pattern di controllo SpreadsheetItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISpreadsheetItemProvider, incluse informazioni su proprietà e metodi.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo SpreadsheetItem
- Automazione interfaccia utente, pattern di controllo SpreadsheetItem
- Automazione interfaccia utente, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implementazione del pattern di controllo SpreadsheetItem di automazione interfaccia utente
- Pattern di controllo SpreadsheetItem
- pattern di controllo, ISpreadsheetItemProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente SpreadsheetItem
- pattern di controllo, SpreadsheetItem
- interfacce, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047232"
---
# <a name="spreadsheetitem-control-pattern"></a>Pattern di controllo SpreadsheetItem

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **SpreadsheetItem** viene usato per esporre le proprietà di una cella in un foglio di calcolo o in un altro documento basato su griglia.

Il pattern di controllo **SpreadsheetItem** è strettamente correlato al pattern di controllo [GridItem](uiauto-implementinggriditem.md) . i controlli che implementano il pattern di controllo **SpreadsheetItem** devono anche implementare il pattern di controllo GridItem. I controlli possono anche implementare il pattern di controllo [TableItem](uiauto-implementingtableitem.md) , se appropriato. Per esempi di controlli che implementano questi pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **SpreadsheetItem** , tenere presenti le linee guida e le convenzioni seguenti:

-   Quando si implementano i metodi [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) e [**ISpreadsheetItemProvider:: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , fare riferimento alla documentazione di [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Questi metodi restituiscono matrici per consentire ai provider di supportare più annotazioni in una singola cella.
-   Alcuni tipi di annotazioni non richiedono un'implementazione completa dell'interfaccia [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Ad esempio, un indicatore di errore di ortografia semplice può essere rappresentato con [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) che restituisce un identificatore di attributo di testo di [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) restituisce un valore null.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Membri obbligatori per **ISpreadsheetItemProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .



| Membri obbligatori                                                                         | Tipo di membro | Note                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Proprietà    | L'implementazione di una proprietà della [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) separata è necessaria perché la proprietà [value](value-property.md) di una cella restituisce in genere il valore calcolato della cella. La proprietà della **Formula** deve essere **null** se non è impostata alcuna formula. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Metodo      | Restituisce una matrice di provider di elementi che fanno riferimento alle annotazioni collegate a questa cella. I puntatori all'interno della matrice possono essere null se un'annotazione non dispone di un provider collegato.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Metodo      | Restituisce una matrice di identificatori del tipo di annotazione che descrivono le annotazioni in questa cella. La matrice deve avere le stesse dimensioni della matrice restituita da [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).                                         |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo foglio di calcolo](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 