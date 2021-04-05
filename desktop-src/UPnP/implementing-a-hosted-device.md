---
title: Implementazione di un dispositivo ospitato
description: L'host del dispositivo con la tecnologia UPnP implementa i protocolli UPnP di base per l'individuazione, la descrizione, il controllo e la gestione degli eventi.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713576"
---
# <a name="implementing-a-hosted-device"></a>Implementazione di un dispositivo ospitato

L'host dispositivo con tecnologia UPnP implementa i protocolli UPnP principali: individuazione, descrizione, controllo ed eventi. Lo sviluppatore che implementa un dispositivo ospitato deve solo fornire:

-   Una descrizione del dispositivo e dei relativi servizi.
-   Implementazione della funzionalità del dispositivo.

Ad esempio, lo sviluppatore di un dispositivo clock deve fornire descrizioni di dispositivi e servizi basati su UPnP e un'implementazione delle funzioni di clock, ad esempio la conservazione del tempo, l'impostazione dell'ora e la risposta alle query per l'ora corrente. Host del dispositivo:

-   Annuncia il dispositivo in base al protocollo di individuazione UPnP.
-   Risponde alle query per la descrizione del dispositivo.
-   Instrada le richieste di controllo alla parte del codice del dispositivo che implementa le funzioni Clock.
-   Mantiene le sottoscrizioni di eventi ai servizi.
-   Invia notifiche degli eventi ai sottoscrittori quando lo stato del servizio viene modificato.

 

 




