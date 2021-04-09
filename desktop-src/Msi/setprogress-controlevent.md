---
description: Il programma di installazione usa l'evento seprogress per pubblicare informazioni sullo stato di avanzamento dell'installazione.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: ControlEvent di avanzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967904"
---
# <a name="setprogress-controlevent"></a>ControlEvent di avanzamento

Il programma di installazione usa l'evento seprogress per pubblicare informazioni sullo stato di avanzamento dell'installazione. Un controllo [ProgressBar](progressbar-control.md) o un [controllo Billboard](billboard-control.md) deve sottoscrivere l'evento tramite la [tabella EventMapping](eventmapping-table.md) assegnando un nome all'azione di cui viene indicato lo stato di avanzamento. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) . Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [ProgressBar](progressbar-control.md) in una finestra di dialogo non modale sottoscrive questo evento usando l'attributo [Progress](progress-control-attribute.md) per ricevere le informazioni sullo stato di avanzamento.

 

 



