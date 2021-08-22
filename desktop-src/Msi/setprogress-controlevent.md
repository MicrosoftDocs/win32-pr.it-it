---
description: Il programma di installazione usa l'evento SetProgress per pubblicare informazioni sullo stato di avanzamento dell'installazione.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e36ecf5851713d7460f8f249b77871439c628f2adfce516aea29db52ad7942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625081"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent

Il programma di installazione usa l'evento SetProgress per pubblicare informazioni sullo stato di avanzamento dell'installazione. Un [controllo ProgressBar o](progressbar-control.md) un controllo Control [deve](billboard-control.md) sottoscrivere l'evento tramite la tabella [EventMapping](eventmapping-table.md) assegnando un nome all'azione il cui stato di avanzamento è indicato. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita a livello di interfaccia utente di [*base,*](b-gly.md) [*interfaccia utente*](r-gly.md)ridotta o [*interfaccia utente*](f-gly.md) completa. Per informazioni sui livelli dell'interfaccia utente, [Interfaccia utente livelli.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo ProgressBar](progressbar-control.md) in una finestra di dialogo non modali sottoscrive questo evento usando l'attributo [Progress](progress-control-attribute.md) per ricevere le informazioni sullo stato di avanzamento.

 

 



