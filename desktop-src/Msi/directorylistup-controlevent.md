---
description: Questo evento notifica al controllo DirectoryList che l'utente vuole selezionare l'elemento padre della directory corrente. Per informazioni correlate, vedere Finestra di dialogo Sfoglia.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: Controllo DirectoryListUpEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99fb0731a06f30cf788e3565e0988bf5b20ebce7abec8be351f4d1fe9d2aab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086181"
---
# <a name="directorylistup-controlevent"></a>Controllo DirectoryListUpEvent

Questo evento notifica al controllo [DirectoryList che](directorylist-control.md) l'utente vuole selezionare l'elemento padre della directory corrente. Per informazioni correlate, vedere [Finestra di dialogo Sfoglia](browse-dialog.md).

Questo evento deve essere pubblicato da un [controllo PushButton](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che lo sottoscrive. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere Livelli [Interfaccia utente.](user-interface-levels.md)

Se la directory corrente è la directory radice dell'unità, un evento DirectoryListUp disabilita tutti gli altri controlli che pubblicano un evento DirectoryListUp.

## <a name="published-by"></a>Pubblicato da

[Elenco directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) nella stessa finestra di dialogo modale di DirectoryList viene usato per attivare l'esecuzione di istruzioni nel percorso.

 

 



