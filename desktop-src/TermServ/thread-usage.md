---
title: Utilizzo di thread
description: È consigliabile ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22959c6950458c95670d71479a2efe04fdafea765048508b9bd371b0a215064d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869521"
---
# <a name="thread-usage"></a>Utilizzo di thread

I thread offrono un modo pratico per consentire a un'applicazione di ottimizzare l'utilizzo delle risorse della CPU in un sistema, in particolare in una configurazione con più processori. In un ambiente Servizi Desktop remoto, tuttavia, più utenti possono eseguire applicazioni multithreading e tutti i thread per tutti gli utenti si concorreranno per le risorse centrali della CPU del sistema. A questo scopo, è necessario ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente e multiprocessore Servizi Desktop remoto ambiente. Sebbene un'applicazione multithreading progettata in modo non adeguato con thread inattivi o sprecati possa essere eseguita in modo adeguato in un computer client, la stessa applicazione potrebbe non avere prestazioni adeguate in un server Servizi Desktop remoto multiutente.

 

 




