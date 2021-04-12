---
title: Pattern di controllo foglio di calcolo
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISpreadsheetProvider, incluse informazioni sui metodi.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Spreadsheet
- Automazione interfaccia utente, pattern di controllo foglio di calcolo
- Automazione interfaccia utente, ISpreadsheetProvider
- ISpreadsheetProvider
- implementazione del pattern di controllo Spreadsheet di automazione interfaccia utente
- pattern di controllo foglio di calcolo
- pattern di controllo, ISpreadsheetProvider
- pattern di controllo, implementazione del foglio di calcolo di automazione
- pattern di controllo, foglio di calcolo
- interfacce, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338327"
---
# <a name="spreadsheet-control-pattern"></a>Pattern di controllo foglio di calcolo

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluse informazioni sui metodi. Alla fine della panoramica sono elencati collegamenti ad altro materiale di riferimento. Il pattern di controllo **Spreadsheet** viene usato per esporre il contenuto di un foglio di calcolo o di un altro documento basato su griglia.

Il pattern di controllo del **foglio di calcolo** è strettamente correlato al pattern di controllo [Grid](uiauto-implementinggrid.md) ; i controlli che implementano il pattern di controllo del **foglio di calcolo** devono implementare anche il pattern di controllo Grid. I controlli possono anche implementare il pattern di controllo [Table](uiauto-implementingtable.md) , se appropriato. Per esempi di controlli che implementano questi pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Spreadsheet** , tenere presenti le linee guida e le convenzioni seguenti:

-   Se un foglio di calcolo implementa l'interfaccia [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , le relative celle devono implementare l'interfaccia [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .
-   Il metodo [**ISpreadsheetProvider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) ha lo scopo di fornire lo stesso tipo di spostamento che un'applicazione può fornire con una funzionalità **di salto all'etichetta** . Molti programmi di fogli di calcolo consentono a determinate celle di assegnare un nome descrittivo o un'etichetta. **GetItemByName** consente al client di cercare una cella in base al nome descrittivo. Questo metodo non deve recuperare le celle che contengono il testo del nome perché i risultati possono essere estremamente ambigui. Se il programma di foglio di calcolo consente a più celle nello stesso foglio di calcolo di avere lo stesso nome descrittivo o etichetta, il comportamento di automazione interfaccia utente Microsoft non è definito.

## <a name="required-members-for-ispreadsheetprovider"></a>Membri obbligatori per **ISpreadsheetProvider**

Il metodo seguente è necessario per implementare l'interfaccia [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .



| Membri obbligatori                                                       | Tipo di membro | Note |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 