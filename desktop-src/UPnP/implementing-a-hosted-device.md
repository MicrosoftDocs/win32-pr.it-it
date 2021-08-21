---
title: Implementazione di un dispositivo ospitato
description: L'host del dispositivo con tecnologia UPnP implementa l'individuazione, la descrizione, il controllo e l'evento dei protocolli UPnP di base.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fd12788c40d21dc84e896f1aba83085b440b86fbb54b68b4fbcfddbbe910c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008051"
---
# <a name="implementing-a-hosted-device"></a>Implementazione di un dispositivo ospitato

L'host del dispositivo con tecnologia UPnP implementa i protocolli UPnP principali: individuazione, descrizione, controllo e gestione degli eventi. Lo sviluppatore che implementa un dispositivo ospitato deve solo fornire:

-   Descrizione del dispositivo e dei relativi servizi.
-   Implementazione della funzionalità del dispositivo.

Ad esempio, lo sviluppatore di un dispositivo orologio deve fornire descrizioni dei servizi e dei dispositivi basati su UPnP e un'implementazione delle funzioni di orologio, ad esempio mantenere l'ora, impostare l'ora e rispondere alle query per l'ora corrente. L'host del dispositivo:

-   Annuncia il dispositivo in base al protocollo di individuazione UPnP.
-   Risponde alle query per la descrizione del dispositivo.
-   Instrada le richieste di controllo alla parte del codice del dispositivo che implementa le funzioni di clock.
-   Gestisce le sottoscrizioni di eventi ai servizi.
-   Invia notifiche degli eventi ai sottoscrittori quando lo stato del servizio cambia.

 

 




