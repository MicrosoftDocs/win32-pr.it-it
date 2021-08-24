---
description: Un mailslot è un meccanismo per le comunicazioni interprocesso unidireli (IPC). Le applicazioni possono archiviare i messaggi in un mailslot. Il proprietario di mailslot può recuperare i messaggi archiviati in tale cartella.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72a4bc50c2cb563894ce9b7c616f9ae86cd9ae6e4abb966c78475c504c75f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716831"
---
# <a name="mailslots"></a>Mailslot

Un *mailslot* è un meccanismo per le comunicazioni interprocesso unidireli (IPC). Le applicazioni possono archiviare i messaggi in un mailslot. Il proprietario di mailslot può recuperare i messaggi archiviati in tale cartella. Questi messaggi vengono in genere inviati in rete a un computer specifico o a tutti i computer in un dominio specificato. Un *dominio* è un gruppo di workstation e server che condividono un nome di gruppo.

-   [Informazioni su Mailslot](about-mailslots.md)
-   [Uso di Mailslot](using-mailslots.md)
-   [Informazioni di riferimento su Mailslot](mailslot-reference.md)

È possibile scegliere di usare [named pipe o](named-pipes.md) Windows [socket](/windows/desktop/WinSock/windows-sockets-start-page-2) anziché mailslot per le comunicazioni interprocesso. Le named pipe sono un modo semplice per due processi di scambiare messaggi. I mailslot, d'altra parte, sono un modo semplice per un processo di trasmettere messaggi a più processi. Una considerazione importante è che i mailslot trasmittenti di messaggi tramite datagrammi. Un *datagramma* è un piccolo pacchetto di informazioni che la rete invia lungo la rete. Analogamente a una trasmissione radiotelevisa, un datagramma non offre alcuna conferma della ricezione; non è possibile garantire che sia stato ricevuto un datagramma. Proprio come i danni, gli edifici di grandi dimensioni o i segnali che interferiscono possono causare la perdita di un segnale radio o tv, esistono elementi che possono impedire a un datagramma di raggiungere una destinazione specifica. Le named pipe sono simili a chiamate telefoniche: si parla solo con una parte, ma si sa che il messaggio viene ricevuto.

 

 
