---
description: Il \_32.dll WS2 fornisce le funzionalità per la creazione di oggetti evento sia per le applicazioni che per i provider di servizi, anche se nella maggior parte dei casi gli oggetti evento verranno creati dalle applicazioni.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Creazione di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307000"
---
# <a name="creating-event-objects"></a>Creazione di oggetti evento

Il \_32.dll WS2 fornisce le funzionalità per la creazione di oggetti evento sia per le applicazioni che per i provider di servizi, anche se nella maggior parte dei casi gli oggetti evento verranno creati dalle applicazioni. I servizi oggetto evento vengono resi disponibili per i provider di servizi Windows Sockets tramite [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) semplicemente come un meccanismo pratico per qualsiasi elaborazione interna che può trarre vantaggio dallo stesso. Si noti che l'handle dell'oggetto evento è valido solo nel contesto del processo chiamante. Negli ambienti Windows la realizzazione degli oggetti evento avviene tramite i servizi eventi nativi forniti dal sistema operativo.

 

 



