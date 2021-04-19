---
description: Questo evento notifica al controllo Directory che è necessario creare una nuova cartella; viene creata la nuova cartella e viene selezionato il campo nome della cartella per la modifica.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: ControlEvent DirectoryListNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319971"
---
# <a name="directorylistnew-controlevent"></a>ControlEvent DirectoryListNew

Questo evento notifica al [controllo Directory](directorylist-control.md) che è necessario creare una nuova cartella; viene creata la nuova cartella e viene selezionato il campo nome della cartella per la modifica. Il nome predefinito della nuova cartella può essere creato nella [tabella UIText](uitext-table.md). Immettere "NewFolder" nella colonna chiave. Immettere il valore per il nome predefinito della nuova cartella nella colonna di testo. Questo valore deve essere nel formato di un tipo di dati della colonna [filename](filename.md) e utilizzare la \| sintassi LFN di SFN. Se questo valore non è presente nella tabella UIText o non è un valore valido, il programma di installazione userà il valore predefinito "FLDR \| New Folder". Per informazioni correlate, vedere [finestra di dialogo Sfoglia](browse-dialog.md).

Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Si noti che se questo ControlEvent viene chiamato nuovamente quando una nuova cartella esiste già, non verrà creata una seconda nuova cartella. In questo caso, la chiamata a DirectoryListNew consente di selezionare il nome della nuova cartella esistente per la modifica.

## <a name="published-by"></a>Pubblicato da

[Elenco di directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Per attivare la creazione di una nuova cartella, viene usato un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale dell'elenco di directory.

 

 



