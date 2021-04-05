---
title: Quali sono le azioni di base dell'API del punto di controllo
description: Tutti i punti di controllo eseguono le seguenti attività.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e2db09aa8283034da20dc1bd2dc877bf0e5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713528"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Quali sono le azioni di base dell'API del punto di controllo?

Tutti i punti di controllo eseguono le attività seguenti:

-   Trovare i dispositivi basati su UPnP disponibili sulla rete.
-   Determinare quali di questi dispositivi sono di interesse.
-   Inviare le richieste di controllo ai dispositivi di interesse e ricevere gli eventi generati dai dispositivi.

Un'applicazione deve innanzitutto individuare i dispositivi basati su UPnP disponibili sulla rete eseguendo una ricerca. Poiché i criteri di ricerca definiti dall'architettura UPnP sono piuttosto ampi, l'applicazione potrebbe trovare più dispositivi del necessario. Pertanto, l'applicazione deve esaminare le caratteristiche dei dispositivi che sono stati individuati per determinare quali più corrispondono ai criteri di ricerca. L'applicazione può quindi emettere richieste di controllo a tali dispositivi.

Le sezioni seguenti descrivono come eseguire queste operazioni usando l'API del punto di controllo con la tecnologia UPnP:

-   [Ricerca di dispositivi](finding-devices.md)
-   [Descrizione dei dispositivi](describing-devices.md)
-   [Controllo dei dispositivi](controlling-devices.md)

Per la documentazione dettagliata su ogni interfaccia nell'API del punto di controllo, vedere [riferimento all'API del punto](control-point-api-with-upnp-technology-reference.md)di controllo.

 

 




