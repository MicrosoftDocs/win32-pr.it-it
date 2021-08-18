---
description: I personal computer che eseguono Microsoft Windows spesso hanno numerose connessioni di rete, ad esempio più schede di interfaccia di rete (NIC) connesse a reti diverse o una connessione di rete fisica e una connessione remota.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Network Location Awareness Service Provider (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7378aff6f51f2785671f1d424a4721f9cd77fad22d60554746f9427d7f24f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132094"
---
# <a name="network-location-awareness-service-provider-nla"></a>Network Location Awareness Service Provider (NLA)

I personal computer che eseguono Microsoft Windows spesso hanno numerose connessioni di rete, ad esempio più schede di interfaccia di rete (NIC) connesse a reti diverse o una connessione di rete fisica e una connessione remota. Windows I socket sono stati in grado di enumerare le interfacce di rete disponibili per un certo periodo di tempo, ma alcune informazioni critiche sulle connessioni di rete in precedenza non erano disponibili. Sono incluse informazioni quali la rete logica a cui è collegato un computer Windows o se più interfacce sono connesse alla stessa rete.

Il provider di servizi NLA (Network Location Awareness), comunemente noto come NLA, consente alle applicazioni Windows Sockets 2 di identificare la rete logica a cui è collegato un computer Windows. Inoltre, NLA consente alle Windows Sockets di identificare l'interfaccia di rete fisica in cui una determinata applicazione ha salvato informazioni specifiche. L'autenticazione a livello di rete viene implementata Windows provider di servizi di risoluzione dei nomi Windows Sockets 2.

 

 



