---
title: Gestione dello stato sul server tra le chiamate
description: Spesso è necessario mantenere lo stato sul server tra le chiamate RPC separate \ 8212. l'uso di handle di contesto è il modo migliore per eseguire questa operazione. Di seguito sono riportate alcune parole sulla modalità di funzionamento interna degli handle di contesto per la comprensione del funzionamento ottimale del contesto.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC (Remote Procedure Call), procedure consigliate, gestione dello stato tra le chiamate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00090fb317cba8c33e7b60ac81762d7d21dd4dc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707186"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Gestione dello stato sul server tra le chiamate

Spesso è necessario mantenere lo stato sul server tra chiamate RPC separate, usando gli handle di contesto è il modo migliore per eseguire questa operazione. Di seguito sono riportate alcune parole sulla modalità di funzionamento interna degli handle di contesto per la comprensione del funzionamento ottimale del contesto.

Il client non riceve mai lo stato mantenuto nel server. La maggior parte delle volte lo stato sul server è un puntatore a un blocco di memoria e il client non ha informazioni su di esso. Tutte le ricevute del client sono un numero univoco di grandi dimensioni, con altre informazioni associate, che il server invia al client e che rappresenta il punto di gestione del contesto in tutte le operazioni successive. Ogni volta che il client fa riferimento a un handle aperto, invia il numero elevato ricevuto dal server al momento dell'apertura dell'handle di contesto.

Il server tiene traccia di tutti i numeri elevati inviati a un client. Quando il server riceve un numero elevato che rappresenta un handle di contesto, Cerca il numero nell'insieme di handle di contesto validi e in attesa per il client e trova il contesto lato server corrispondente a un numero elevato specificato. Viene passato alla routine del server. Se il numero elevato non viene trovato, \_ \_ \_ \_ viene generata un'eccezione di mancata corrispondenza del contesto RPC X SS e propagata al client.

Il corollari di questa progettazione è il seguente:

-   Un handle di contesto è valido solo nel contesto della sessione client/server esistente. Non può essere passato a un altro client.
-   Un handle di contesto diventa non valido se il server viene riavviato o perde la connessione al client.
-   Il client non è in grado di interpretare il punto di gestione del contesto rappresentato nel server. Per un client, tutti gli handle di contesto sono semplicemente numeri elevati.

Se il client ha esito negativo, il server riceve una notifica e pulisce i relativi handle di contesto usando il meccanismo di esecuzione.

 

 




