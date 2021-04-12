---
title: Linee guida hardware periferiche
description: Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono garantire che il software dei driver di dispositivo forzi la disabilitazione del reindirizzamento del dispositivo usando criteri di sistema o criteri di gruppo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396463"
---
# <a name="peripheral-hardware-guidelines"></a>Linee guida hardware periferiche

Per un client Connessione Desktop remoto (RDC), il server di host sessione Desktop remoto (host sessione Desktop remoto) è il computer locale. Di conseguenza, i dispositivi come le unità disco e le stampanti collegate al server vengono visualizzati come dispositivi locali per un client. Al contrario, le unità e le stampanti collegate a un terminale client possono sembrare dispositivi remoti, a seconda delle opzioni selezionate per la connessione, del server utilizzato e della versione del software client utilizzata.

Sebbene la versione iniziale di Servizi Desktop remoto non supportasse le applicazioni che inviano l'output direttamente alle porte seriali, parallele e audio collegate al terminale client, le versioni correnti consentono a tali dispositivi di apparire come dispositivi locali per le applicazioni in esecuzione nella sessione di Servizi Desktop remoto.

Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono garantire che il software dei driver di dispositivo forzi la disabilitazione del reindirizzamento del dispositivo usando criteri di sistema o criteri di gruppo.

 

 




