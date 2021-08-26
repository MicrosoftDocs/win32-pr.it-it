---
description: Il controllo SelectionTree usa l'evento SelectionBrowse per generare una finestra di dialogo Sfoglia che consente di modificare il percorso dell'elemento evidenziato.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70d7c50e69921a5fefe7cff3c88c2351cacdecda42a164e8334c9afb3977bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040611"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent

Il [controllo SelectionTree usa](selectiontree-control.md) l'evento SelectionBrowse per generare una finestra di dialogo **Sfoglia** che consente di modificare il percorso dell'elemento evidenziato.

Questo evento deve essere pubblicato da un [controllo PushButton](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che lo sottoscrive. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

Tutti i controlli che pubblicano un evento SelectionBrowse vengono disabilitati se è stata selezionata una funzionalità già installata, non configurabile o non selezionata per l'installazione locale. Per essere configurabile, la funzionalità deve avere una [proprietà pubblica](public-properties.md) immessa nel campo Directory della \_ tabella [Funzionalità](feature-table.md).

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nome della finestra di dialogo da generare.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) nella stessa finestra di dialogo modale di SelectionTree usa questo evento per attivare la **finestra di** dialogo Sfoglia.

 

 



