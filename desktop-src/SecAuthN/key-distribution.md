---
description: La tecnica di autenticazione della chiave privata non spiega in che modo il client e il server ottengono la chiave di sessione privata da usare nelle sessioni.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribuzione delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd39f9cd5e219ac1e6339c0a6c3e7b9a19dc2680c21e948bdb979af791719a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013331"
---
# <a name="key-distribution"></a>Distribuzione delle chiavi

La tecnica di autenticazione della chiave privata non spiega in che modo il client e il server ottengono la chiave di sessione [*privata*](../secgloss/s-gly.md) da usare nelle sessioni. Se sono persone, potrebbero incontrarsi in segreto e accettare la chiave. Se tuttavia il client è un programma in esecuzione in una workstation e il server è un servizio in esecuzione in un server di rete, questo metodo non funzionerà.

Un client dovrà comunicare con molti server e avrà bisogno di chiavi diverse per ognuno di essi. Un server comunica con molti client e richiede chiavi diverse anche per ognuno di essi. Se ogni client necessita di una chiave diversa per ogni server e ogni server necessita di una chiave diversa per ogni client, la distribuzione delle chiavi diventa un problema. Inoltre, la necessità di archiviare e proteggere molte chiavi in molti computer crea un enorme rischio per la sicurezza.

Il nome del protocollo [*Kerberos suggerisce*](../secgloss/k-gly.md) la soluzione al problema della distribuzione delle chiavi. Kerberos (o Cerberus) era una figura nella classica mitologia del greco, un cane a tre teste che continuava a vivere intrusi dall'ingresso nell'oltretomba. Come la mitica protezione, il protocollo Kerberos ha tre teste: un client, un server e una terza parte attendibile per mediare tra di essi. L'intermediario attendibile in questo protocollo è Centro distribuzione chiavi (KDC).

Il KDC è un servizio in esecuzione in un server fisicamente sicuro. Gestisce un database con le informazioni sull'account per tutte [*le entità di sicurezza*](../secgloss/s-gly.md) nella relativa area di autenticazione. Un'area di autenticazione è l'equivalente Kerberos di un dominio in Windows.

Insieme ad altre informazioni su ogni entità di sicurezza, il KDC archivia una chiave crittografica nota solo all'entità e al KDC. Si tratta della [*chiave master*](../secgloss/m-gly.md) usata negli scambi tra ogni entità di sicurezza e KDC. Nella maggior parte delle implementazioni del protocollo Kerberos, questa chiave master viene derivata usando una funzione [*hash*](../secgloss/h-gly.md) dalla password di un'entità di sicurezza.

Quando un client vuole creare una connessione sicura con un server, il client inizia inviando una richiesta al KDC, non al server che vuole raggiungere. Il KDC crea e invia [](../secgloss/s-gly.md) al client una chiave di sessione univoca per il client e un server da usare per l'autenticazione reciproca. Il KDC ha accesso sia alla chiave master del client che alla chiave master del server. Il KDC crittografa la copia del server della chiave di sessione usando la chiave master del server e la copia del client usando la chiave master del client.

Il KDC potrebbe svolgere il proprio ruolo di intermediario attendibile inviando la chiave di sessione direttamente a ognuna delle entità di sicurezza coinvolte, ma in pratica questa procedura non funzionerà, per diversi motivi. Al contrario, il KDC invia entrambe le chiavi di sessione crittografate al client. La chiave di sessione per il server è inclusa in un [ticket di sessione.](session-tickets.md)

 

 
