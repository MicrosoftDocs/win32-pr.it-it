---
description: Il ControlEvent SpawnDialog notifica al programma di installazione di creare un elemento figlio di una finestra di dialogo modale mantenendo la finestra di dialogo in esecuzione.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: ControlEvent SpawnDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305960"
---
# <a name="spawndialog-controlevent"></a>ControlEvent SpawnDialog

Il ControlEvent SpawnDialog notifica al programma di installazione di creare un elemento figlio di una finestra di dialogo modale mantenendo la finestra di dialogo in esecuzione.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa che rappresenta il nome della nuova finestra di dialogo.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per creare una finestra di dialogo figlio, ad esempio "annullare?" dell'applicazione di condivisione.

 

 



