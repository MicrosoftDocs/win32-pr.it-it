---
description: La maggior parte delle estensioni dello spazio dei nomi è un subset dello spazio dei nomi Shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea8ed12d4333ac2c4de7973410a822fefea827be769bbe7ccf754890712e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968840"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi

La maggior parte delle estensioni dello spazio dei nomi è un subset dello spazio dei nomi Shell. Quando si crea un punto di giunzione, come descritto in Specifica della posizione di un'estensione dello spazio dei nomi, Windows Explorer consente agli utenti di spostarsi [all'interno e all'interno dell'estensione](nse-junction.md)dello spazio dei nomi come qualsiasi altra cartella. Tuttavia, è anche possibile usare Windows Explorer per visualizzare solo il contenuto dell'estensione dello spazio dei nomi. Questa opzione di visualizzazione viene talvolta definita visualizzazione *radice.* Anche se non comunemente usate, le viste radice potrebbero essere preferibili alle visualizzazioni normali per alcuni tipi di estensioni.

Con una visualizzazione radice, viene creata una nuova istanza di Windows Explorer che visualizza il contenuto dell'estensione come spazio dei nomi separato. La visualizzazione albero di una visualizzazione radice mostra solo le cartelle che fanno parte dell'estensione. Gli utenti non possono spostarsi da una visualizzazione radice ad altre parti dello spazio dei nomi shell.

Le estensioni vengono implementate nello stesso modo per le viste radice come per le visualizzazioni normali. L'unica differenza consiste nel modo in cui il contenuto dell'estensione viene visualizzato da Windows Explorer. È anche possibile avere visualizzazioni normali e radice della stessa estensione.

Per aprire una visualizzazione di un'estensione, è necessario avviare un'istanza di Explorer.exe con un flag /root. Esistono diversi modi per avviare una visualizzazione radice, a seconda della natura dell'estensione.

-   [Come usare un punto di giunzione per aprire una vista radice](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Come usare un file di collegamento per aprire una visualizzazione radice](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Come visualizzare una visualizzazione radice di un file](how-to-display-a-rooted-view-of-a-file.md)

 

 



