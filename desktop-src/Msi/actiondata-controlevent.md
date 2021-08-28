---
description: Il programma di installazione usa questo evento per pubblicare i dati sull'azione più recente. I dati possono essere visualizzati in una finestra di dialogo da un controllo di testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c280bbd2c0a184ec281e4401037687893942b4c344824b20a59c410b59fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105481"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent

Il programma di installazione usa questo evento per pubblicare i dati sull'azione più recente. I dati possono essere visualizzati in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita a livello di interfaccia utente di [*base,*](b-gly.md)interfaccia [*utente*](r-gly.md)ridotta [*o interfaccia utente*](f-gly.md) completa. Per informazioni sui livelli dell'interfaccia utente, [vedere Interfaccia utente Livelli.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

I sottoscrittori vengono nascosti all'avvio di una nuova azione e visualizzati quando i nuovi dati dell'azione arrivano dal programma di installazione.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo Di testo](text-control.md) in una finestra di dialogo non modali sottoscrive questo evento tramite la tabella [EventMapping](eventmapping-table.md). [L'attributo text control](text-control-attribute.md) è elencato nel campo Attributi di questa tabella per ricevere i dati dell'azione corrente. Usato in genere per visualizzare i nomi dei file copiati durante la copia del file.

 

 



