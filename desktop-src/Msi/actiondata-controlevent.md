---
description: Il programma di installazione utilizza questo evento per pubblicare i dati nell'ultima azione. I dati possono essere visualizzati in una finestra di dialogo da un controllo di testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ControlEvent ActionData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311090"
---
# <a name="actiondata-controlevent"></a>ControlEvent ActionData

Il programma di installazione utilizza questo evento per pubblicare i dati nell'ultima azione. I dati possono essere visualizzati in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) . Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

I sottoscrittori sono nascosti quando viene avviata una nuova azione che viene visualizzata quando i nuovi dati di azione arrivano dal programma di installazione.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo di testo](text-control.md) in una finestra di dialogo non modale sottoscrive questo evento tramite la [tabella EventMapping](eventmapping-table.md). L' [attributo di controllo Text](text-control-attribute.md) è elencato nel campo Attributes della tabella per ricevere i dati dell'azione corrente. Usato in genere per visualizzare i nomi dei file copiati durante la copia del file.

 

 



