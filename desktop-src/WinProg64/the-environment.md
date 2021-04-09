---
title: Ambiente
description: Gli sviluppatori che lavorano sulle applicazioni per Windows a 64 bit troveranno l'ambiente di sviluppo praticamente identico all'ambiente di sviluppo per Windows a 32 bit.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- ambiente di sviluppo programmazione Windows a 64 bit
- ambiente a 64 bit programmazione Windows
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, ambiente di sviluppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044383"
---
# <a name="the-environment"></a>Ambiente

Gli sviluppatori che lavorano sulle applicazioni per Windows a 64 bit troveranno l'ambiente di sviluppo praticamente identico all'ambiente di sviluppo per Windows a 32 bit. Le API esistenti sono state modificate laddove necessario per consentire loro di riflettere la precisione della piattaforma in cui sono in esecuzione. Il risultato è la semplicità e una breve curva di apprendimento per lo sviluppatore: la scrittura di codice per Windows a 64 bit è esattamente come la scrittura di codice per Windows a 32 bit.

I file di intestazione di Windows supportano i nuovi tipi di dati che consentono a puntatori e variabili associate a puntatore di riflettere la precisione della piattaforma. Ciò significa che gli sviluppatori possono compilare una singola base di origine per l'esecuzione a livello nativo in Windows a 32 bit o a 64 bit. Questa strategia consente di ridurre i costi di sviluppo di applicazioni che sfruttano l'hardware a 64 bit, ad esempio processori AMD Opteron o Athlon64 o processori Intel Itanium.

Se si adottano le nuove convenzioni del tipo di dati appena possibile, sarà necessario più tempo per rendere le applicazioni disponibili a 64 bit. Se si modifica il codice, è necessario modificare le definizioni dei dati nello stesso momento. Testare l'applicazione in Windows a 32 bit, eseguirla tramite il compilatore a 64 bit (descritto negli [strumenti](the-tools.md)) e l'applicazione sarà pronta per essere testata quando si dispone dell'hardware a 64 bit appropriato.

 

 




