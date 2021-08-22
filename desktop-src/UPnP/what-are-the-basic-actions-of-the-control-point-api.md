---
title: Quali sono le azioni di base dell'API del punto di controllo
description: Tutti i punti di controllo eseguono le attività seguenti.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a102c389a41b32fd7a79bf749ce38f1267912c3993e2461adac9b6730ea92325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513641"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Quali sono le azioni di base dell'API del punto di controllo?

Tutti i punti di controllo eseguono le attività seguenti:

-   Trovare i dispositivi basati su UPnP disponibili nella rete.
-   Determinare quali di questi dispositivi sono di interesse.
-   Inviare richieste di controllo ai dispositivi di interesse e ricevere eventi generati dai dispositivi.

Un'applicazione deve prima trovare i dispositivi basati su UPnP disponibili nella rete eseguendo una ricerca. Poiché i criteri di ricerca definiti dall'architettura UPnP sono piuttosto ampi, l'applicazione potrebbe trovare più dispositivi di quelli necessari. Pertanto, l'applicazione deve esaminare le caratteristiche dei dispositivi trovati per determinare quali corrispondono maggiormente ai criteri di ricerca. L'applicazione può quindi mettere richieste di controllo a tali dispositivi.

Le sezioni seguenti descrivono come eseguire queste operazioni usando l'API Punto di controllo con la tecnologia UPnP:

-   [Ricerca di dispositivi](finding-devices.md)
-   [Descrizione dei dispositivi](describing-devices.md)
-   [Controllo dei dispositivi](controlling-devices.md)

Per una documentazione dettagliata su ogni interfaccia nell'API del punto di controllo, vedere Informazioni di riferimento [sull'API del punto di controllo](control-point-api-with-upnp-technology-reference.md).

 

 




