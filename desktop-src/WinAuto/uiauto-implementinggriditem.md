---
title: Pattern di controllo GridItem
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IGridItemProvider, incluse le informazioni sulle proprietà. Il pattern di controllo GridItem viene usato per supportare singoli controlli figlio di contenitori che implementano IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo GridItem
- Automazione interfaccia utente, pattern di controllo GridItem
- Automazione interfaccia utente, IGridItemProvider
- IGridItemProvider
- implementazione di pattern di controllo GridItem di automazione interfaccia utente
- Pattern di controllo GridItem
- pattern di controllo, IGridItemProvider
- pattern di controllo, implementazione di GridItem di automazione interfaccia utente
- pattern di controllo, GridItem
- interfacce, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709694"
---
# <a name="griditem-control-pattern"></a>Pattern di controllo GridItem

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), incluse le informazioni sulle proprietà. Il pattern di controllo **GridItem** viene usato per supportare singoli controlli figlio di contenitori che implementano [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IGridItemProvider**](#required-members-for-igriditemprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **GridItem** , tenere presenti le linee guida e le convenzioni seguenti:

-   Le coordinate della griglia sono in base zero. Le coordinate della cella in alto a sinistra sono infatti (0, 0).
-   Le celle unite segnaleranno le proprietà di [**riga**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) e [**colonna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) in base alla cella di ancoraggio sottostante, come definito dal provider di automazione interfaccia utente Microsoft. In genere si tratterà della riga o della colonna più in alto e più a sinistra.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) non fornisce la manipolazione attiva della griglia, ad esempio l'Unione o la suddivisione di celle.
-   I controlli che implementano [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) possono in genere essere attraversati, ovvero un client di automazione interfaccia utente può spostarsi sui controlli adiacenti usando la tastiera.

## <a name="required-members-for-igriditemprovider"></a>Membri obbligatori per **IGridItemProvider**

Per l'implementazione dell'interfaccia [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) sono necessarie le proprietà seguenti.



| Membri obbligatori                                                  | Tipo di membro | Note |
|-------------------------------------------------------------------|-------------|-------|
| [**Riga**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | Proprietà    | nessuno  |
| [**Colonna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | Proprietà    | nessuno  |
| [**RowSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | Proprietà    | nessuno  |
| [**ColumnSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | Proprietà    | nessuno  |
| [**ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | Proprietà    | nessuno  |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo Grid](uiauto-implementinggrid.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




