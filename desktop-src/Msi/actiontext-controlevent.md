---
description: Il programma di installazione utilizza questo evento per pubblicare il nome dell'azione corrente. Il nome può essere visualizzato in una finestra di dialogo da un controllo di testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ControlEvent ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967303"
---
# <a name="actiontext-controlevent"></a>ControlEvent ActionText

Il programma di installazione utilizza questo evento per pubblicare il nome dell'azione corrente. Il nome può essere visualizzato in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) . Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

I sottoscrittori vengono visualizzati quando i nuovi dati di stato arrivano dal programma di installazione.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo di testo](text-control.md) in una finestra di dialogo non modale sottoscrive questo evento tramite la [tabella EventMapping](eventmapping-table.md). L' [attributo del controllo testo](text-control-attribute.md) deve essere elencato nel campo attributi di questa tabella per ricevere il nome dell'azione corrente.

 

 



