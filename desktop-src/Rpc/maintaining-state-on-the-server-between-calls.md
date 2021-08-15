---
title: Gestione dello stato nel server tra le chiamate
description: Spesso è necessario mantenere lo stato nel server tra chiamate RPC separate \ 8212; l'uso degli handle di contesto è il modo migliore per eseguire questa operazione. Alcune parole sul funzionamento interno degli handle di contesto consentono di comprendere quando gli handle di contesto funzionano meglio.
ms.assetid: f76ec489-f48e-473d-b519-3ac143d41fa4
keywords:
- RPC remote procedure call , procedure consigliate, gestione dello stato tra le chiamate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e564acbb4748cd76988c1b064a58ede2169d3d20da4033774f3141883a7193bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928586"
---
# <a name="maintaining-state-on-the-server-between-calls"></a>Gestione dello stato nel server tra le chiamate

Spesso è necessario mantenere lo stato nel server tra chiamate RPC separate. L'uso di handle di contesto è il modo migliore per eseguire questa operazione. Alcune parole sul funzionamento interno degli handle di contesto consentono di comprendere quando gli handle di contesto funzionano meglio.

Il client non riceve mai lo stato mantenuto nel server. Molto spesso lo stato nel server è un puntatore a un blocco di memoria e il client non dispone di informazioni su di esso. Tutto il client riceve un numero univoco elevato, con altre informazioni associate, che il server invia al client e che rappresenta l'handle di contesto in tutte le operazioni successive. Ogni volta che il client fa riferimento a un handle aperto, invia il numero elevato ricevuto dal server quando tale handle di contesto è stato aperto.

Il server tiene traccia di tutti i numeri di grandi dimensioni inviati a un client. Quando il server riceve un numero elevato che rappresenta un handle di contesto, cerca il numero nella raccolta di handle di contesto validi in attesa per il client e trova il contesto sul lato server corrispondente a un numero elevato specificato. Viene passato alla routine del server. Se il numero elevato non viene trovato, viene generata un'eccezione \_ MISMATCH RPC X SS CONTEXT e \_ \_ \_ propagata al client.

Le corollarie di questa progettazione sono le seguenti:

-   Un handle di contesto è valido solo nel contesto della sessione client/server esistente. Non può essere passato a un altro client.
-   Un handle di contesto diventa non valido se il server viene riavviato o in caso contrario perde la connessione al client.
-   Il client non può interpretare ciò che l'handle di contesto rappresenta nel server. Per un client, tutti gli handle di contesto sono semplicemente numeri grandi.

Se il client ha esito negativo, il server riceverà una notifica e pulirà i relativi handle di contesto usando il meccanismo di run-down.

 

 




