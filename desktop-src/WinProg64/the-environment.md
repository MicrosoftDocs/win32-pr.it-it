---
title: Ambiente
description: Gli sviluppatori che lavorano su applicazioni per Windows a 64 bit troveranno l'ambiente di sviluppo praticamente identico all'ambiente di sviluppo per le applicazioni a 32 bit Windows.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- programmazione Windows a 64 bit dell'ambiente di sviluppo
- programmazione Windows a 64 bit
- Guida alla programmazione Windows a 64 bit Windows programmazione a 64 bit , ambiente di sviluppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69580d6537c832abaf51b20a553c4e4e788a6013bdfc14a8002f60de9872da62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734131"
---
# <a name="the-environment"></a>Ambiente

Gli sviluppatori che lavorano su applicazioni per Windows a 64 bit troveranno l'ambiente di sviluppo praticamente identico all'ambiente di sviluppo per le applicazioni a 32 bit Windows. Le API esistenti sono state modificate se necessario per consentire loro di riflettere la precisione della piattaforma in cui sono in esecuzione. Il risultato è la semplicità e una breve curva di apprendimento per lo sviluppatore: la scrittura di codice per Windows a 64 bit è simile alla scrittura di codice per le Windows a 32 bit.

I Windows di intestazione supportano nuovi tipi di dati che consentono ai puntatori e alle variabili associate al puntatore di riflettere la precisione della piattaforma. Ciò significa che gli sviluppatori possono compilare una singola base di origine per l'esecuzione in modo nativo in Windows a 32 bit o a 64 bit Windows. Questa strategia riduce i costi di sviluppo di applicazioni che sfruttano hardware a 64 bit, ad esempio processori AMD Opteron o Athlon64 o processori Intel Itanium.

Sarà più tempo per rendere le applicazioni pronte a 64 bit se si adottano le nuove convenzioni del tipo di dati appena possibile. Se si modifica il codice, è necessario modificare le definizioni dei dati contemporaneamente. Testare l'applicazione in un Windows a 32 bit, eseguirla tramite il compilatore a 64 bit (descritto in [Strumenti](the-tools.md)) e l'applicazione sarà pronta per il test quando si dispone dell'hardware a 64 bit appropriato.

 

 




