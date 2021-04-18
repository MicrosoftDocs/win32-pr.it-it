---
description: Questa finestra di dialogo modale consente agli utenti di selezionare determinati elementi.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Finestra di dialogo di selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319433"
---
# <a name="selection-dialog"></a>Finestra di dialogo di selezione

Questa finestra di dialogo modale consente agli utenti di selezionare determinati elementi.

Una finestra di dialogo di selezione contiene un [controllo SelectionTree](selectiontree-control.md) che pubblica più ControlEvents. Comunemente questi ControlEvents sono sottoscritti da controlli di [testo](text-control.md), [icona](icon-control.md)o [bitmap](bitmap-control.md) che visualizzano una descrizione, le dimensioni, il percorso e l'icona dell'elemento evidenziato.

Nella finestra di dialogo è presente un [controllo pulsante](pushbutton-control.md) che pubblica il [ControlEvent SelectionBrowse](selectionbrowse-controlevent.md) e genera una finestra di [dialogo di esplorazione](browse-dialog.md). Il controllo Browse consente all'utente di selezionare una directory.

L'albero di selezione viene popolato solo dopo la chiamata dell' [azione CostInitialize](costinitialize-action.md) e dell' [azione CostFinalize secondo](costfinalize-action.md) .

Una finestra di dialogo di selezione viene comunemente usata per selezionare le funzionalità. Le funzionalità sono elencate come elementi in un controllo SelectionTree ed etichettate con la breve stringa di testo visualizzata nella colonna title della [tabella Feature](feature-table.md). La stringa di testo nella colonna Descrizione della tabella delle funzionalità viene pubblicata come [SelectionDescription ControlEvent](selectiondescription-controlevent.md) e visualizzata da un [controllo di testo](text-control.md) nella finestra di dialogo di selezione. Il controllo albero di selezione pubblica anche l'handle per l'icona dell'elemento evidenziato.

 

 



