---
description: Consente all'autore di specificare la modalità o le modalità di convalida durante una reinstallazione e mentre è in esecuzione la finestra di dialogo corrente.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ControlEvent ReinstallMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311697"
---
# <a name="reinstallmode-controlevent"></a>ControlEvent ReinstallMode

ReinstallMode ControlEventallows l'autore per specificare la modalità o le modalità di convalida durante una reinstallazione e durante l'esecuzione della finestra di dialogo corrente.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md) o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md)e richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funziona con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa. Per un elenco di valori possibili, vedere proprietà [**REINSTALLMODE**](reinstallmode.md) .

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Questo evento è associato a un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale. Lo stesso controllo [pulsante](pushbutton-control.md) deve essere associato anche a un ControlEvent di [Reinstallazione](reinstall-controlevent.md) .

 

 



