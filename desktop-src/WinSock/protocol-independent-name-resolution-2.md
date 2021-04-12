---
description: Risoluzione dei nomi indipendente dal protocollo e Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Risoluzione dei nomi Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343476"
---
# <a name="protocol-independent-name-resolution"></a>Risoluzione dei nomi Protocol-Independent

Per lo sviluppo di un'applicazione client/server indipendente dal protocollo, esistono due requisiti di base per quanto riguarda la risoluzione dei nomi e la registrazione:

-   Capacità della metà del server dell'applicazione (servizio) di registrare la propria esistenza entro (o diventare accessibile) uno o più spazi dei nomi.
-   La capacità dell'applicazione client di trovare il servizio in uno spazio dei nomi e di ottenere il protocollo di trasporto e le informazioni di indirizzamento richiesti.

Per chi è abituato allo sviluppo di applicazioni basate su TCP/IP, questo può sembrare poco più che cercare un indirizzo host e quindi usare un numero di porta concordato. Tuttavia, altri schemi di rete consentono di individuare il percorso del servizio, il protocollo utilizzato per il servizio e altri attributi in fase di esecuzione. Per supportare la vasta gamma di funzionalità disponibili nei servizi dei nomi esistenti, l'interfaccia Windows Sockets 2 adotta il modello descritto negli argomenti in questa sezione.

In questa sezione vengono descritte le funzionalità di risoluzione dei nomi indipendenti dal protocollo disponibili per gli sviluppatori Winsock. Nell'elenco seguente vengono descritti gli argomenti di questa sezione:

-   [Modello di risoluzione dei nomi](name-resolution-model-2.md)
-   [Riepilogo delle funzioni di risoluzione dei nomi](summary-of-name-resolution-functions-2.md)
-   [Strutture dei dati di risoluzione dei nomi](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



