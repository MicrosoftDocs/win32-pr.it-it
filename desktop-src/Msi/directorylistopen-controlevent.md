---
description: Questo evento seleziona ed evidenzia una directory nel controllo DirectoryList che l'utente ha scelto di aprire. Per informazioni correlate, vedere Finestra di dialogo Sfoglia.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1453ffd42e0763ec747f02f7030818eaba3d533e5dfcca4570c13596efdcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947325"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent

Questo evento seleziona ed evidenzia una directory nel controllo [DirectoryList](directorylist-control.md) che l'utente ha scelto di aprire. Per informazioni correlate, vedere [Finestra di dialogo Sfoglia](browse-dialog.md).

Questo evento deve essere pubblicato da un [controllo PushButton](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che lo sottoscrive. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere Livelli [Interfaccia utente.](user-interface-levels.md)

Se non è stata selezionata alcuna directory nel controllo [DirectoryList](directorylist-control.md), un evento DirectoryListOpen disabilita tutti gli altri controlli che pubblicano un evento DirectoryListOpen.

## <a name="published-by"></a>Pubblicato da

[Elenco directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue alcuna azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) nella stessa finestra di dialogo modale di DirectoryList viene usato per attivare l'esecuzione di istruzioni nel percorso.

 

 



