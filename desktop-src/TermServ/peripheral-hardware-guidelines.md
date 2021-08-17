---
title: Linee guida per l'hardware periferico
description: Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono assicurarsi che il software del driver di dispositivo forza la disabilitazione del reindirizzamento del dispositivo tramite criteri di sistema o criteri di gruppo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0cbe39010eaa59d4207ad28722521793fe33a04f9d06591f21f8ac381940235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756270"
---
# <a name="peripheral-hardware-guidelines"></a>Linee guida per l'hardware periferico

Per un client Connessione Desktop remoto (RDC), il server host sessione Desktop remoto (Host sessione Desktop remoto) è il computer locale. Di conseguenza, i dispositivi, ad esempio le unità disco e le stampanti collegate al server, vengono visualizzati come dispositivi locali per un client. Al contrario, le unità e le stampanti collegate a un terminale client possono sembrare dispositivi remoti, a seconda delle opzioni selezionate per la connessione, del server usato e della versione del software client usata.

Sebbene la versione iniziale di Servizi Desktop remoto non supporti le applicazioni che inviano l'output direttamente alle porte seriali, parallele e sonore collegate al terminale client, le versioni correnti consentono a questi dispositivi di apparire come dispositivi locali alle applicazioni in esecuzione nella sessione Servizi Desktop remoto.

Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono assicurarsi che il software del driver di dispositivo forza la disabilitazione del reindirizzamento del dispositivo tramite criteri di sistema o criteri di gruppo.

 

 




