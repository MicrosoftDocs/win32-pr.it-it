---
description: Questo evento seleziona ed evidenzia una directory nel controllo Directory che l'utente ha scelto di aprire. Per informazioni correlate, vedere finestra di dialogo Sfoglia.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: ControlEvent DirectoryListOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234354"
---
# <a name="directorylistopen-controlevent"></a>ControlEvent DirectoryListOpen

Questo evento seleziona ed evidenzia una directory nel [controllo Directory](directorylist-control.md) che l'utente ha scelto di aprire. Per informazioni correlate, vedere [finestra di dialogo Sfoglia](browse-dialog.md).

Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Se non è stata selezionata alcuna directory nel [controllo Directory](directorylist-control.md), un evento DirectoryListOpen Disabilita tutti gli altri controlli che pubblicano un evento DirectoryListOpen.

## <a name="published-by"></a>Pubblicato da

[Elenco di directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue alcuna azione nei Sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale in cui si trova l'elenco di directory viene usato per attivare l'istruzione/routine nel percorso.

 

 



