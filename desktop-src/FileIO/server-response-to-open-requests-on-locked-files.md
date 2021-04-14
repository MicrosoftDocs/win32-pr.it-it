---
description: È possibile ridurre al minimo l'impatto dell'applicazione su altri client e l'impatto che hanno sull'applicazione concedendo il maggior numero possibile di condivisione, richiedendo il livello di accesso minimo necessario e usando il blocco opportunistico meno intrusivo adatto all'applicazione.
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: Risposta server per l'apertura di richieste su file bloccati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526857"
---
# <a name="server-response-to-open-requests-on-locked-files"></a>Risposta server per l'apertura di richieste su file bloccati

Il ciclo di vita di un blocco opportunistico include tre intervalli di tempo distinti. Durante ogni, il server determina con diversi significa la reazione a una richiesta da un client di aprire un file bloccato da un altro client. In generale, è possibile ridurre al minimo l'impatto dell'applicazione su altri client e l'impatto che hanno sull'applicazione concedendo il maggior numero possibile di condivisione, richiedendo il livello di accesso minimo necessario e usando il blocco opportunistico meno intrusivo adatto all'applicazione.

Il primo è il periodo dopo il quale il server apre un file per un client, ma prima di concedere un blocco. Durante questo periodo di tempo non esiste alcun blocco nel file e il server dipende dalla condivisione, dalle modalità di accesso e dal tipo di blocco opportunistico richiesto per determinare la reazione a un'altra richiesta di apertura dello stesso file. Ad esempio, se si apre il file in questione per l'accesso in scrittura, è possibile impedire la concessione di blocchi opportunistici che consentono l'accesso in lettura alla cache ad altri client. L'intervallo di tempo prima che il Server conceda un blocco si trova in genere nell'intervallo di millisecondi, ma potrebbe essere più lungo.

Dopo la concessione del blocco opportunistico, il server esamina il blocco per determinare la risposta del server a una richiesta aperta su un file bloccato. Anche in questo caso, il modo in cui l'applicazione ha aperto il file e il tipo di blocco che possiede influiscono sulle modalità di risposta del server. Per ulteriori informazioni sul modo in cui il server risponde in ogni caso, vedere [tipi di blocchi opportunistici](types-of-opportunistic-locks.md).

Infine, è presente l'intervallo dopo il quale il server determina che il blocco deve essere interrotto (terminato), ma prima che l'applicazione completi la propria reazione all'interruzione. A seconda del tipo di blocco, l'applicazione può eseguire il downgrade del blocco a un livello inferiore o a nessuno. L'applicazione può anche chiudere il file e il blocco. Durante questo periodo di tempo, il server rimane in sospeso per tutte le richieste provenienti da altri client per aprire il file bloccato in precedenza. Questo intervallo di tempo può variare da millisecondi a decine di secondi. Per ulteriori informazioni, vedere la pagina relativa alla [suddivisione dei blocchi opportunistici](breaking-opportunistic-locks.md).

 

 



