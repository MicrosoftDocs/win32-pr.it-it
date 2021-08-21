---
description: È necessario considerare in particolare i mittenti o i ricevitori PGM multihomed. Questa pagina descrive le considerazioni e fornisce linee guida per le procedure di programmazione consigliate.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multihoming e PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e19ab149c8068c1a13f2c8089a567157618ef7287e8ef632145e5b934d626c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112085"
---
# <a name="multihoming-and-pgm"></a>Multihoming e PGM

È necessario considerare in particolare i mittenti o i ricevitori PGM multihomed. Questa pagina descrive le considerazioni e fornisce linee guida per le procedure di programmazione consigliate.

## <a name="multihomed-pgm-sender"></a>Mittente PGM multihomed

Quando un'applicazione non riesce a specificare un'interfaccia al momento della chiamata alla [**funzione connect,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene usata la prima interfaccia disponibile. Se non è disponibile alcuna interfaccia, la **connessione non** riesce.

Quando un'applicazione specifica un'interfaccia usando l'opzione [](/windows/desktop/api/winsock/nf-winsock-bind) socket [RM \_ SET \_ SEND \_ IF,](socket-options.md) viene eseguito in modo implicito un tentativo di associazione a tale interfaccia tramite TCP/IP e ha esito negativo se TCP/IP ha esito negativo nella richiesta di associazione. Se l'interfaccia viene impostata tramite RM SET SEND IF più volte, è applicabile solo \_ \_ \_ l'ultimo set di interfacce.

Windows I socket mantengono l'interfaccia impostata e, se tale interfaccia scompare, la sessione viene disconnessa.

## <a name="multihomed-pgm-receiver"></a>Ricevitore PGM multihomed

Quando un'applicazione non riesce a specificare un'interfaccia al momento della chiamata alla funzione [**di**](/windows/desktop/api/Winsock2/nf-winsock2-listen) ascolto, viene usata l'interfaccia predefinita. Se non è disponibile alcuna interfaccia, [**l'associazione non**](/windows/desktop/api/winsock/nf-winsock-bind) riesce.

Quando un'applicazione specifica una o più interfacce su cui restare in ascolto, usando [RM \_ ADD RECEIVE \_ \_ IF](socket-options.md), Windows Sockets tenta di eseguire l'associazione all'interfaccia o alle interfacce richieste usando TCP/IP. Qualsiasi errore da TCP/IP causa l'esito negativo della richiesta. A differenza del caso del mittente PGM, l'aggiunta di un'interfaccia di ricezione più volte comporta la registrazione degli ascolto in tutte le interfacce aggiunte correttamente. Usare l'opzione socket RM \_ DEL RECEIVE IF per \_ \_ arrestare l'ascolto su un'interfaccia.

Windows I socket non mantengono lo stato di più interfacce di ascolto specificate e si basano invece su TCP/IP per eseguire questa operazione. Una volta in corso una sessione, tuttavia, Windows Sockets tiene traccia dell'interfaccia in ingresso per tale sessione e, se tale interfaccia scompare, Windows Sockets disconnette la sessione.

 

 



