---
description: L'32.dll Ws2 offre funzionalità per la creazione di oggetti evento sia alle applicazioni che ai provider di servizi, anche se nella maggior parte dei casi gli oggetti evento \_ verranno creati dalle applicazioni.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Creazione di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab867e6398db4b5c97303c8739431d7baaca311daf8d103f4375721e96a864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051699"
---
# <a name="creating-event-objects"></a>Creazione di oggetti evento

L'32.dll Ws2 offre funzionalità per la creazione di oggetti evento sia alle applicazioni che ai provider di servizi, anche se nella maggior parte dei casi gli oggetti evento \_ verranno creati dalle applicazioni. I servizi oggetto evento vengono resi disponibili ai provider di servizi Windows Sockets tramite [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) semplicemente come meccanismo di praticità per qualsiasi elaborazione interna che possa trarre vantaggio dallo stesso. Si noti che l'handle dell'oggetto evento è valido solo nel contesto del processo chiamante. Negli Windows la realizzazione di oggetti evento è tramite i servizi eventi nativi forniti dal sistema operativo.

 

 



