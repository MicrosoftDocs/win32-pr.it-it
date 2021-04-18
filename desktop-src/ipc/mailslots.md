---
description: Un inserimento/espulsione è un meccanismo per le comunicazioni interprocesso unidirezionali (IPC). Le applicazioni possono archiviare i messaggi in un inserimento/espulsione. Il proprietario di inserimento/espulsione è in grado di recuperare i messaggi archiviati.
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317319"
---
# <a name="mailslots"></a>Mailslot

Un *inserimento/espulsione* è un meccanismo per le comunicazioni interprocesso unidirezionali (IPC). Le applicazioni possono archiviare i messaggi in un inserimento/espulsione. Il proprietario di inserimento/espulsione è in grado di recuperare i messaggi archiviati. Questi messaggi vengono in genere inviati in rete a un computer specifico o a tutti i computer in un dominio specificato. Un *dominio* è un gruppo di workstation e server che condividono un nome di gruppo.

-   [Informazioni su mailslot](about-mailslots.md)
-   [Uso di mailslot](using-mailslots.md)
-   [Riferimento a inserimento/espulsione](mailslot-reference.md)

È possibile scegliere di utilizzare [named pipe](named-pipes.md) o [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) anziché mailslot per le comunicazioni interprocesso. Le named pipe rappresentano un modo semplice per scambiare messaggi tra due processi. Mailslot, d'altra parte, rappresentano un modo semplice per la trasmissione di messaggi a più processi da parte di un processo. Una considerazione importante è che mailslot trasmette i messaggi usando datagrammi. Un *datagramma* è un piccolo pacchetto di informazioni che la rete invia lungo il cavo. Analogamente a una trasmissione radiofonica o televisiva, un datagramma non offre alcuna conferma della ricezione. non esiste alcun modo per garantire che sia stato ricevuto un datagramma. Così come le montagne, le grandi costruzioni o i segnali che interferiscono potrebbero causare la perdita di un segnale radio o televisivo, è possibile impedire a un datagramma di raggiungere una destinazione specifica. Le named pipe sono analoghe alle chiamate telefoniche: si comunica solo a una parte, ma si sa che il messaggio viene ricevuto.

 

 
