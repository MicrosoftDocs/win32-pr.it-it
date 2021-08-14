---
description: Questo evento notifica al controllo DirectoryList che è necessario creare una nuova cartella. crea la nuova cartella e seleziona il campo del nome della cartella per la modifica.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281835954c947e4bcaaf6e4e2019cbd422151e6cca39b83fa84a0abe0db010cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378901"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent

Questo evento notifica al [controllo DirectoryList che](directorylist-control.md) è necessario creare una nuova cartella. crea la nuova cartella e seleziona il campo del nome della cartella per la modifica. Il nome predefinito della nuova cartella può essere creato nella tabella [UIText](uitext-table.md). Immettere "NewFolder" nella colonna Chiave. Immettere il valore per il nome predefinito della nuova cartella nella colonna Testo. Questo valore deve essere nel formato di un tipo di dati della colonna [Filename](filename.md) e usare la sintassi SFN \| LFN. Se questo valore non è presente nella tabella UIText o è un valore non valido, il programma di installazione usa il valore predefinito "Fldr \| New Folder". Per informazioni correlate, vedere [Finestra di dialogo Sfoglia.](browse-dialog.md)

Questo evento deve essere pubblicato da un [controllo PushButton](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive l'evento. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Interfaccia utente Levels.](user-interface-levels.md)

Si noti che se questo ControlEvent viene chiamato di nuovo quando esiste già una nuova cartella, non verrà creata una seconda nuova cartella. In questo caso, la chiamata a DirectoryListNew seleziona il nome della nuova cartella esistente per la modifica.

## <a name="published-by"></a>Pubblicato da

[Elenco directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento .

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) nella stessa finestra di dialogo modale di DirectoryList viene usato per attivare la creazione di una nuova cartella.

 

 



