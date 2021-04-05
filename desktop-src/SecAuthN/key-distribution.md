---
description: La tecnica di autenticazione con chiave privata non spiega in che modo il client e il server ottengono la chiave della sessione segreta da usare nelle sessioni tra loro.
ms.assetid: 90ab0359-5079-49e9-809c-0c0005cc61bf
title: Distribuzione delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a2968e8b7b978bc7b325d65b4a2acf08e1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757010"
---
# <a name="key-distribution"></a>Distribuzione delle chiavi

La tecnica di autenticazione con chiave privata non spiega in che modo il client e il server ottengono la [*chiave della sessione*](../secgloss/s-gly.md) segreta da usare nelle sessioni tra loro. Se sono persone, possono incontrarsi in segreto e accettare la chiave. Tuttavia, se il client è un programma in esecuzione su una workstation e il server è un servizio in esecuzione su un server di rete, il metodo non funzionerà.

Un client desidera comunicare con molti server e dovrà avere chiavi diverse per ognuno di essi. Un server comunica con molti client e necessita di chiavi diverse per ognuno di essi. Se ogni client necessita di una chiave diversa per ogni server e ogni server necessita di una chiave diversa per ogni client, la distribuzione delle chiavi diventa un problema. Inoltre, la necessità di archiviare e proteggere molte chiavi in molti computer comporta un enorme rischio per la sicurezza.

Il nome del [*protocollo Kerberos*](../secgloss/k-gly.md) suggerisce la soluzione al problema di distribuzione delle chiavi. Kerberos (o Cerbero) era una figura della mitologia greca classica, un cane feroce e a tre punte che ha mantenuto gli intrusi nell'entrare nel mondo. Come il mitico Guard, il protocollo Kerberos è costituito da tre intestazioni: un client, un server e una terza parte attendibile per la mediazione. L'intermediario attendibile in questo protocollo è il Centro distribuzione chiavi (KDC).

Il KDC è un servizio in esecuzione su un server fisicamente protetto. Gestisce un database con le informazioni sull'account per tutte le [*entità di sicurezza*](../secgloss/s-gly.md) nell'area di autenticazione. Un'area di autenticazione è l'equivalente Kerberos di un dominio di Windows.

Insieme ad altre informazioni su ogni entità di sicurezza, il KDC archivia una chiave crittografica nota solo per l'entità e il KDC. Si tratta della [*chiave master*](../secgloss/m-gly.md) utilizzata negli scambi tra ciascuna entità di sicurezza e il KDC. Nella maggior parte delle implementazioni del protocollo Kerberos, questa chiave master viene derivata utilizzando una funzione [*hash*](../secgloss/h-gly.md) della password di un'entità di sicurezza.

Quando un client desidera creare una connessione protetta con un server, il client inizia inviando una richiesta al KDC, non al server che desidera raggiungere. Il KDC crea e invia al client una chiave di [*sessione*](../secgloss/s-gly.md) univoca per il client e un server da usare per l'autenticazione reciproca. Il KDC può accedere sia alla chiave master del client che alla chiave master del server. Il KDC crittografa la copia del server della chiave della sessione utilizzando la chiave master del server e la copia del client utilizzando la chiave master del client.

Il KDC può svolgere il proprio ruolo di intermediario attendibile inviando la chiave della sessione direttamente a ognuna delle entità di sicurezza interattive, ma in pratica questa procedura non funzionerà per diversi motivi. Al contrario, il KDC invia entrambe le chiavi della sessione crittografata al client. La chiave della sessione per il server è inclusa in un [ticket di sessione](session-tickets.md).

 

 
