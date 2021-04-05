---
description: Le funzioni di installazione includono la funzionalità di Accodamento file.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Code di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967863"
---
# <a name="file-queues"></a>Code di file

Le funzioni di installazione includono la funzionalità di Accodamento file. Una coda di file è un elenco di operazioni di copia, ridenominazione ed eliminazione di file. Queste operazioni possono essere inviate alla coda in qualsiasi ordine. Quando viene eseguito il commit della coda, le operazioni vengono elaborate come batch, in ordine di tipo di operazione.

Nelle sezioni seguenti viene illustrata una coda e viene illustrato come utilizzarla quando si crea un'applicazione di installazione. Viene inoltre illustrato l'ordine in cui le operazioni di file accodate vengono elaborate durante il commit della coda e le notifiche inviate dalla coda a una routine di callback in ogni fase.

-   [Informazioni sulle code di file](about-file-queues.md)
-   [Uso di code di file](using-file-queues.md)
-   [Riferimento alla coda di file](file-queue-reference.md)

 

 



