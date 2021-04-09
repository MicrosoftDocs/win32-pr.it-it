---
description: Questo evento notifica al controllo Directory che l'utente desidera selezionare l'elemento padre della directory corrente. Per informazioni correlate, vedere finestra di dialogo Sfoglia.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: ControlEvent DirectoryListUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968757"
---
# <a name="directorylistup-controlevent"></a>ControlEvent DirectoryListUp

Questo evento notifica al [controllo Directory](directorylist-control.md) che l'utente desidera selezionare l'elemento padre della directory corrente. Per informazioni correlate, vedere [finestra di dialogo Sfoglia](browse-dialog.md).

Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Se la directory corrente è la directory radice dell'unità, un evento DirectoryListUp Disabilita tutti gli altri controlli che pubblicano un evento DirectoryListUp.

## <a name="published-by"></a>Pubblicato da

[Elenco di directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale in cui si trova l'elenco di directory viene utilizzato per attivare l'esecuzione nel percorso.

 

 



