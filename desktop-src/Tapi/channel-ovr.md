---
description: Ogni riga contiene uno o più canali. I provider di servizi gestiscono in genere il modo in cui i canali vengono esposti come indirizzi a un'applicazione e l'utente finale o il server non richiede una conoscenza specifica dei canali.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canale (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527235"
---
# <a name="channel-telephony-api"></a>Canale (API di telefonia)

Ogni riga contiene uno o più canali. I provider di servizi gestiscono in genere il modo in cui i canali vengono esposti come indirizzi a un'applicazione e l'utente finale o il server non richiede una conoscenza specifica dei canali.

I canali sono identici e pertanto intercambiabili. In POTS (servizio telefonico normale), esiste esattamente un canale su una riga e il canale viene usato esclusivamente per la voce. Con ISDN è possibile che esistano almeno tre canali (e fino a 30) su una riga contemporaneamente.

Ogni canale può avere un proprio indirizzo, il che significa che una linea può avere il numero di indirizzi configurati per i canali. La relazione precisa tra i canali e gli indirizzi esposti a un'applicazione dipende dall'implementazione di un provider di servizi.

Alcuni provider di servizi supportano l'assegnazione di più di un indirizzo a un singolo canale. Nelle linee di PENTOLe sono possibili più indirizzi da parte di vari sistemi, ad esempio la composizione diretta verso l'interno (DID) o la suoneria distinta, ovvero servizi aggiuntivi forniti dall'azienda telefonica.

Molte aziende di grandi dimensioni usano per le chiamate in ingresso. Prima che venga connessa una chiamata, il numero di estensione di destinazione viene segnalato al PBX, che fa sì che l'estensione venga squillata al posto del telefono dell'operatore. Un esempio di suoneria distinta in una casa privata è costituito dal caso in cui gli elementi padre utilizzano un indirizzo, l'altro figlio e un computer fax al terzo. Poiché una sola linea connette la casa alla rete telefonica, tutti i telefoni squillano quando viene visualizzata una chiamata, ma lo schema circolare è diverso a seconda del numero che l'entità chiamante ha composto. Con la suoneria distinta, le persone sanno chi è la chiamata in ingresso e il computer fax risponde alle chiamate riconoscendo il proprio stile di suoneria.

In ISDN i diversi canali B potrebbero non avere indirizzi distinti. Poiché questi canali B potrebbero trovarsi nello stesso indirizzo, è il provider di servizi (e non l'applicazione o una persona che ha composto il numero) che assegna chiamate a questi canali.

 

 



