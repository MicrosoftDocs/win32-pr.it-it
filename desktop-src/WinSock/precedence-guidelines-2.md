---
description: I due (o più) descrittori che fanno riferimento a un socket condiviso possono essere usati in modo indipendente per quanto riguarda l'I/O.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Linee guida per la precedenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129138"
---
# <a name="precedence-guidelines"></a>Linee guida per la precedenza

I due (o più) descrittori che fanno riferimento a un socket condiviso possono essere usati in modo indipendente per quanto riguarda l'I/O. Tuttavia, l'interfaccia Windows Sockets non implementa alcun tipo di controllo di accesso, quindi spetta ai processi che coordinano le operazioni su un socket condiviso. Un utilizzo tipico per i socket condivisi consiste nel disporre di un processo responsabile della creazione di socket e della creazione di connessioni che trasferiscono i socket ad altri processi responsabili dello scambio di informazioni.

La linea guida generale per il supporto di più operazioni in attesa sui socket condivisi è che un provider di servizi è incoraggiato a rispettare tutte le operazioni simultanee sui socket condivisi, in particolare l'operazione più recente su un oggetto Socket. Se necessario, questo può verificarsi a scapito dell'annullamento di alcune delle operazioni precedenti, ma ancora in sospeso, che restituiranno WSAEINTR in questo caso.

 

 



