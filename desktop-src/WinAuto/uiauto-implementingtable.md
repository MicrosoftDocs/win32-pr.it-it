---
title: Pattern di controllo tabella
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di ITableProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Table viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Table
- Automazione interfaccia utente,Pattern di controllo tabella
- Automazione interfaccia utente,ITableProvider
- ITableProvider
- implementazione di Automazione interfaccia utente di controllo tabella
- Pattern di controllo tabella
- pattern di controllo, ITableProvider
- pattern di controllo, implementazione Automazione interfaccia utente tabella
- pattern di controllo,tabella
- interfacce, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb484245ee7c2f982ca6c5624ad108a0c75a4721ba7f6cbdf7a8af8ee2d91881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324136"
---
# <a name="table-control-pattern"></a>Pattern di controllo tabella

Vengono descritte le linee guida e le convenzioni per l'implementazione [**di ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluse informazioni su proprietà e metodi. Il **pattern di** controllo Table viene usato per supportare i controlli che fungono da contenitori per una raccolta di elementi figlio.

Gli elementi figlio dell'elemento contenitore devono implementare [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) ed essere organizzati in un sistema di coordinate logiche bidimensionale che può essere attraversato da righe e colonne. Questo pattern di controllo è analogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) con la distinzione che qualsiasi controllo che implementa [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) deve esporre anche una relazione di intestazione di colonna e/o di riga per ogni elemento figlio. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri necessari per **ITableProvider**](#required-members-for-itableprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il **pattern di controllo Table,** tenere presente le linee guida e le convenzioni seguenti:

-   L'accesso al contenuto delle singole celle è tramite un sistema di coordinate logico bidimensionale o una matrice fornita dall'implementazione simultanea richiesta di [**IGridProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)
-   Un'intestazione di riga o colonna può essere contenuta all'interno di un oggetto tabella oppure essere un oggetto intestazione distinto associato a un oggetto tabella.
-   Le intestazioni di riga e colonna possono includere un'intestazione principale nonché intestazioni di supporto.
    > [!Note]  
    > Questo concetto diventa evidente in un foglio Microsoft Excel in cui un utente ha definito una **colonna Nome.** Questa colonna include ora due intestazioni, tra cui l'intestazione **First name** definita dall'utente e la designazione alfanumerica per tale colonna assegnata dall'applicazione.

     

-   Vedere [Grid Control Pattern (Pattern di controllo griglia)](uiauto-implementinggrid.md) per le funzionalità della griglia correlate.

    L'immagine seguente mostra una tabella con intestazioni di colonna complesse.

    ![tabella con intestazioni di colonna complesse](images/uia-valuepattern-colorpicker.jpg)

    L'immagine seguente mostra una tabella con una proprietà [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambigua.

    ![tabella con una proprietà roworcolumnmajor ambigua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Membri necessari per **ITableProvider**

Per l'implementazione dell'interfaccia [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                                   | Tipo di membro | Note |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Proprietà    | Nessuno  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Metodo      | Nessuno  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Pattern di controllo TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 




