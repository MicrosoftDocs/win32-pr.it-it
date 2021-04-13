---
description: COM+ introduce appartamenti neutri per semplificare la programmazione in ambienti multithread. L'Apartment neutro è il modello preferito per COM+ per i componenti senza interfaccia utente.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Appartamenti neutri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401433"
---
# <a name="neutral-apartments"></a>Appartamenti neutri

COM+ introduce appartamenti neutri per semplificare la programmazione in ambienti multithread. L'Apartment neutro è il modello preferito per COM+ per i componenti senza interfaccia utente.

In passato, per evitare colli di bottiglia, gli sviluppatori COM+ che richiedevano la scalabilità del server dovevano implementare i componenti a thread libero. Tuttavia, i modelli di threading libero sono complicati da implementare perché devono gestire l'accesso con Interlocking. Negli appartamenti neutri gli oggetti seguono le linee guida per gli Apartment a thread multipli ma possono essere eseguiti su qualsiasi tipo di thread. Quando un thread è in esecuzione in un Apartment neutro, il contesto dell'oggetto viene ricevuto senza causare un cambio di thread.

Ogni processo può avere un solo Apartment neutro. Per selezionare un Apartment neutro, usare l'impostazione del registro di sistema seguente:

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

I componenti che dispongono di interfacce utente devono continuare a usare Apartment a thread singolo come modello preferito. Per selezionare un Apartment a thread singolo, usare l'impostazione del registro di sistema seguente:

**ThreadingModel** = Apartment

 

 



