---
title: Gestione della pipe asincrona sul lato client
description: Prima di eseguire una chiamata remota asincrona, il client deve innanzitutto inizializzare l'handle asincrono.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856686"
---
# <a name="client-side-asynchronous-pipe-handling"></a>Gestione della pipe asincrona sul lato client

Prima di eseguire una chiamata remota asincrona, il client deve innanzitutto inizializzare l'handle asincrono. Come per le procedure non pipe, il client chiama una funzione asincrona con l'handle asincrono come primo parametro e usa l'handle asincrono per inviare e ricevere dati della pipe, eseguire una query sullo stato della chiamata e ricevere la risposta.

Il client esegue la chiamata di procedura remota asincrona con l'handle asincrono come primo parametro. Il client può utilizzare questo handle per eseguire una query sullo stato della chiamata e ricevere la risposta. Il modello di pipe asincrono è simmetrico. Le applicazioni client e server inviano e ricevono i dati di pipe in modo attivo (in contrapposizione a RPC sincrona, in cui i dati della pipe vengono inviati e ricevuti passivamente).

Il client invia dati di pipe asincroni chiamando la funzione **push** sulla pipe asincrona appropriata, con la variabile di stato della pipe come primo parametro. Quando la funzione **push** restituisce, il client può modificare o liberare il buffer di invio.

Se il \_ flag di notifica asincrona RPC \_ \_ per \_ INVIO \_ è impostato nell'handle asincrono e se APC vengono usati come meccanismo di notifica, un APC viene accodato quando l'invio della pipe è effettivamente completo. È possibile sfruttare questo meccanismo per implementare il controllo di flusso. Si noti, tuttavia, che se il client esegue il push di un altro buffer prima del completamento del push precedente, il client può, a seconda della velocità dell'operazione di trasferimento, ricevere una sola notifica di invio completo, anziché una notifica per ogni buffer o ogni operazione **push** . Quando il client ha inviato tutti i dati della pipe, effettua una chiamata **push** finale con il numero di elementi impostato su 0.

Il programma client riceve i dati della pipe asincrona chiamando la funzione **pull** sulla pipe asincrona appropriata, con la variabile di stato della pipe come primo parametro. Se non sono disponibili dati della pipe, la funzione **pull** restituisce \_ la \_ \_ chiamata asincrona \_ in sospeso della RPC.

Se il meccanismo di notifica è APC e il server ha restituito \_ la \_ chiamata asincrona RPC S \_ \_ in sospeso, il client deve attendere fino a quando non riceve **RpcReceiveComplete** APC dalla fase di esecuzione prima di chiamare di nuovo **pull** .

 

 




