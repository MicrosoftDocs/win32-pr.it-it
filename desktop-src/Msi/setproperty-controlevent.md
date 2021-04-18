---
description: "La sintassi per l'evento SetProperty è diversa da quella per altri ControlEvents al posto del nome dell'evento. uno inserisce la proprietà tra parentesi quadre: \\[ nome della \\_ proprietà \\] ."
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: Proprietà ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314776"
---
# <a name="setproperty-controlevent"></a>Proprietà ControlEvent

La sintassi per l'evento SetProperty è diversa da quella per altri ControlEvents al posto del nome dell'evento. uno inserisce la proprietà tra parentesi quadre: \[ nome della \_ proprietà \] . L'argomento è il nuovo valore della proprietà. Per annullare la proprietà, l'argomento deve essere {} . Questa operazione è necessaria perché l'argomento è una chiave primaria nella tabella e quindi non può essere null. L'argomento verrà formattato con il metodo FormatText, pertanto l'argomento può contenere qualsiasi espressione che il metodo FormatText è in grado di gestire. I valori delle proprietà vengono valutati al momento del ControlEvent.

Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nuovo valore della proprietà. {} per null.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Controllo [pulsante](pushbutton-control.md) in una finestra di dialogo collegata a questo evento in modo che modifichi una proprietà quando viene eseguito il push del pulsante.

 

 



