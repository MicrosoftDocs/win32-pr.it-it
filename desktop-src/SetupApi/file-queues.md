---
description: Le funzioni di installazione includono la funzionalità della coda di file.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Code di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af071d059ea6862f79927da5321d027257bafb035bc81a3586ed34b8dcd9505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965647"
---
# <a name="file-queues"></a>Code di file

Le funzioni di installazione includono la funzionalità della coda di file. Una coda di file è un elenco di operazioni di copia, ridenominazione ed eliminazione di file. Queste operazioni possono essere inviate alla coda in qualsiasi ordine. Quando viene eseguito il commit della coda, queste operazioni vengono elaborate come batch, in ordine di tipo di operazione.

Le sezioni seguenti illustrano che cos'è una coda e come usarla quando si crea un'applicazione di installazione. Viene illustrato anche l'ordine in cui le operazioni sui file accodati vengono elaborate durante il commit della coda e le notifiche inviate dalla coda a una routine di callback in ogni fase.

-   [Informazioni sulle code di file](about-file-queues.md)
-   [Uso delle code di file](using-file-queues.md)
-   [Informazioni di riferimento sulla coda di file](file-queue-reference.md)

 

 



