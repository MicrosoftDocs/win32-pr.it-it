---
title: Utilizzo di thread
description: È consigliabile ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297881"
---
# <a name="thread-usage"></a>Utilizzo di thread

I thread rappresentano un modo pratico per consentire a un'applicazione di massimizzare l'utilizzo delle risorse della CPU in un sistema, soprattutto in una configurazione a più processori. In un ambiente di Servizi Desktop remoto, tuttavia, più utenti possono eseguire applicazioni multithread e tutti i thread per tutti gli utenti competono per le risorse della CPU centrale del sistema. Tenendo presente questo aspetto, è consigliabile ottimizzare e bilanciare l'utilizzo del thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore. Anche se un'applicazione multithreading progettata in modo non corretto con thread inattivi o sprecati potrebbe funzionare adeguatamente in un computer client, è possibile che la stessa applicazione non venga eseguita correttamente in un server Servizi Desktop remoto multiutente.

 

 




