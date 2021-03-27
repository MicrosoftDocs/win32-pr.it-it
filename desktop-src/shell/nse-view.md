---
description: La maggior parte delle estensioni dello spazio dei nomi è un subset dello spazio dei nomi shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980007"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi

La maggior parte delle estensioni dello spazio dei nomi è un subset dello spazio dei nomi shell. Quando si crea un punto di giunzione, come descritto in [specifica della posizione di un'estensione dello spazio dei nomi](nse-junction.md), Esplora risorse consente agli utenti di spostarsi all'interno e all'esterno dell'estensione dello spazio dei nomi come qualsiasi altra cartella. Tuttavia, è anche possibile usare Esplora risorse per visualizzare solo il contenuto dell'estensione dello spazio dei nomi. Questa opzione di visualizzazione viene a volte definita *visualizzazione radice*. Sebbene non sia comunemente utilizzato, le visualizzazioni radice possono essere preferibili alle visualizzazioni normali per alcuni tipi di estensioni.

Con una visualizzazione con radice, viene creata una nuova istanza di Esplora risorse che Visualizza il contenuto dell'estensione come spazio dei nomi separato. La visualizzazione struttura ad albero di una visualizzazione radice Mostra solo le cartelle che fanno parte dell'estensione. Gli utenti non possono spostarsi da una vista radice ad altre parti dello spazio dei nomi della shell.

Le estensioni vengono implementate nello stesso modo per le visualizzazioni con radice così come sono per le visualizzazioni normali. L'unica differenza è rappresentata dal modo in cui il contenuto dell'estensione viene visualizzato da Esplora risorse. È anche possibile avere viste normali e con radice della stessa estensione.

Per aprire una vista di un'estensione, è necessario avviare un'istanza di Explorer.exe con un flag/root. Esistono diversi modi per avviare una visualizzazione con radice, a seconda della natura dell'estensione.

-   [Come usare un punto di giunzione per aprire una visualizzazione con radice](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Come usare un file di collegamento per aprire una visualizzazione con radice](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Come visualizzare una visualizzazione radice di un file](how-to-display-a-rooted-view-of-a-file.md)

 

 



