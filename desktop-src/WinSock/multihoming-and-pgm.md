---
description: È necessario prestare particolare attenzione a mittenti o ricevitori PGM multihomed. In questa pagina vengono descritte le considerazioni e vengono fornite linee guida per procedure di programmazione ottimali.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multihoming e PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306929"
---
# <a name="multihoming-and-pgm"></a>Multihoming e PGM

È necessario prestare particolare attenzione a mittenti o ricevitori PGM multihomed. In questa pagina vengono descritte le considerazioni e vengono fornite linee guida per procedure di programmazione ottimali.

## <a name="multihomed-pgm-sender"></a>Mittente PGM multihomed

Quando un'applicazione non riesce a specificare un'interfaccia quando chiama la funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , viene usata la prima interfaccia disponibile. Se non è disponibile alcuna interfaccia, la **connessione** ha esito negativo.

Quando un'applicazione specifica un'interfaccia utilizzando l'opzione [RM \_ set \_ Send \_ if](socket-options.md) socket, un tentativo di [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) viene eseguito in modo implicito a tale interfaccia utilizzando TCP/IP e ha esito negativo se TCP/IP non riesce a eseguire la richiesta di binding. Se l'interfaccia viene impostata con RM \_ set \_ Send \_ se più volte, è applicabile solo l'ultimo set di interfacce.

Windows Sockets mantiene l'interfaccia impostata e, se tale interfaccia scompare, la sessione viene disconnessa.

## <a name="multihomed-pgm-receiver"></a>Ricevitore PGM multihomed

Quando un'applicazione non riesce a specificare un'interfaccia quando chiama la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , viene utilizzata l'interfaccia predefinita. Se non è disponibile alcuna interfaccia, l' [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) non riesce.

Quando un'applicazione specifica una o più interfacce su cui restare in ascolto utilizzando [RM \_ Add \_ Receive \_ if](socket-options.md), Windows Sockets tenta di eseguire l'associazione all'interfaccia o alle interfacce richieste tramite TCP/IP. Qualsiasi errore di TCP/IP causa la mancata riuscita della richiesta. A differenza del caso del mittente PGM, l'aggiunta di un'interfaccia di ricezione più volte comporta la pubblicazione in attesa di tutte le interfacce aggiunte correttamente. Usare l' \_ \_ \_ opzione di ricezione del socket If di RM per arrestare l'attesa su un'interfaccia.

Windows Sockets non mantiene lo stato di più interfacce di ascolto specificate e si basa invece su TCP/IP. Quando è in corso una sessione, tuttavia, Windows Sockets tiene traccia dell'interfaccia in ingresso per tale sessione. se l'interfaccia scompare, Windows Sockets disconnette la sessione.

 

 



