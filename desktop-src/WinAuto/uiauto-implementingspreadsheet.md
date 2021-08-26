---
title: Pattern di controllo foglio di calcolo
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ISpreadsheetProvider, incluse le informazioni sui metodi.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo del foglio di calcolo
- Automazione interfaccia utente,pattern di controllo foglio di calcolo
- Automazione interfaccia utente,ISpreadsheetProvider
- ISpreadsheetProvider
- implementazione di Automazione interfaccia utente di controllo del foglio di calcolo
- Pattern di controllo del foglio di calcolo
- pattern di controllo,ISpreadsheetProvider
- pattern di controllo, implementazione di Automazione interfaccia utente foglio di calcolo
- pattern di controllo, foglio di calcolo
- interfacce,ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7991937f1530e28ed85227fbe19be13b628f9722d5609367e2f483c86a2bb70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098281"
---
# <a name="spreadsheet-control-pattern"></a>Pattern di controllo foglio di calcolo

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluse le informazioni sui metodi. Alla fine della panoramica sono elencati collegamenti ad altro materiale di riferimento. Il **pattern di** controllo Foglio di calcolo viene usato per esporre il contenuto di un foglio di calcolo o di un altro documento basato su griglia.

Il **pattern di** controllo Foglio di calcolo è strettamente correlato al pattern di [controllo](uiauto-implementinggrid.md) Grid. Anche i controlli che implementano il pattern di controllo **Spreadsheet** devono implementare il pattern di controllo Grid. I controlli possono anche implementare il pattern di controllo [Table,](uiauto-implementingtable.md) se appropriato. Per esempi di controlli che implementano questi pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern **di controllo Spreadsheet,** tenere presente le linee guida e le convenzioni seguenti:

-   Se un foglio di calcolo implementa [**l'interfaccia ISpreadsheetProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) le relative celle devono implementare [**l'interfaccia ISpreadsheetItemProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider)
-   Il [**metodo ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) è progettato per fornire lo stesso tipo di navigazione che un'applicazione potrebbe fornire con una funzionalità **Passa** ad etichetta. Molti fogli di calcolo consentono a celle specifiche di assegnare un nome descrittivo o un'etichetta. **GetItemByName** consente al client di cercare una cella in base al nome descrittivo. Questo metodo non deve recuperare le celle che contengono il testo del nome perché i risultati possono essere altamente ambigui. Se il programma di foglio di calcolo consente a più celle nello stesso foglio di calcolo di avere lo stesso nome descrittivo o etichetta, il comportamento di Microsoft Automazione interfaccia utente non è definito.

## <a name="required-members-for-ispreadsheetprovider"></a>Membri obbligatori per **ISpreadsheetProvider**

Il metodo seguente è necessario per implementare [**l'interfaccia ISpreadsheetProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)



| Membri obbligatori                                                       | Tipo di membro | Note |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 