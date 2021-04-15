---
title: Pattern di controllo Table
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITableProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Table viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Table
- Automazione interfaccia utente, pattern di controllo Table
- Automazione interfaccia utente, ITableProvider
- ITableProvider
- implementazione di pattern di controllo Table di automazione interfaccia utente
- Pattern di controllo Table
- pattern di controllo, ITableProvider
- pattern di controllo, implementazione della tabella di automazione interfaccia utente
- pattern di controllo, tabella
- interfacce, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104554478"
---
# <a name="table-control-pattern"></a>Pattern di controllo Table

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **Table** viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.

Gli elementi figlio dell'elemento contenitore devono implementare [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) ed essere organizzati in un sistema di coordinate logico bidimensionale che può essere attraversato da righe e colonne. Questo pattern di controllo è analogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , con la differenza che qualsiasi controllo che implementa [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) deve esporre anche una relazione di intestazione di riga e/o di colonna per ogni elemento figlio. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ITableProvider**](#required-members-for-itableprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Table** , tenere presenti le linee guida e le convenzioni seguenti:

-   L'accesso al contenuto delle singole celle avviene tramite un sistema di coordinate logico bidimensionale o una matrice fornita dall'implementazione simultanea richiesta di [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).
-   Un'intestazione di riga o colonna può essere contenuta all'interno di un oggetto tabella oppure essere un oggetto intestazione distinto associato a un oggetto tabella.
-   Le intestazioni di riga e colonna possono includere un'intestazione principale nonché intestazioni di supporto.
    > [!Note]  
    > Questo concetto diventa evidente in un foglio di calcolo di Microsoft Excel in cui un utente ha definito una colonna con **nome** . Questa colonna include ora due intestazioni, tra cui l'intestazione del **nome** definito dall'utente e la designazione alfanumerica per la colonna assegnata dall'applicazione.

     

-   Vedere [pattern di controllo Grid](uiauto-implementinggrid.md) per la funzionalità della griglia correlata.

    Nell'immagine seguente viene illustrata una tabella con intestazioni di colonna complesse.

    ![tabella con intestazioni di colonna complesse](images/uia-valuepattern-colorpicker.jpg)

    Nell'immagine seguente viene illustrata una tabella con una proprietà [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambigua.

    ![tabella con una proprietà RowOrColumnMajor ambigua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Membri obbligatori per **ITableProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .



| Membri obbligatori                                                   | Tipo di membro | Note |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Proprietà    | nessuno  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Metodo      | nessuno  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




