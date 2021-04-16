---
title: Monitoraggio del sistema
description: Monitoraggio del sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395222"
---
# <a name="monitoring-the-system"></a>Monitoraggio del sistema

Ripristino configurazione di sistema in Windows Vista e in seguito Salva una copia del volume durante la generazione di un punto di ripristino. Per ripristino configurazione di sistema sono necessari almeno 300 MB di spazio libero su disco nell'unità di sistema durante l'installazione.

Ripristino configurazione di sistema in Windows XP esegue il monitoraggio di un set di base di file di sistema e dell'applicazione, archiviando gli Stati di questi file prima che vengano apportate modifiche al sistema. Ripristino configurazione di sistema salva anche uno snapshot completo del registro di sistema e alcuni file di sistema dinamici. Per ripristino configurazione di sistema sono necessari almeno 200 MB di spazio libero su disco nell'unità di sistema durante l'installazione. Quando la quantità di spazio libero su disco scende sotto 50 MB in qualsiasi unità, ripristino configurazione di sistema passa alla modalità standby e interrompe la creazione dei punti di ripristino. Tutti i punti di ripristino vengono eliminati in quel momento. Ripristino configurazione di sistema riattiva e riprende la creazione di punti di ripristino non appena 200 MB di spazio su disco è disponibile nell'unità di sistema. I file monitorati o esclusi dal monitoraggio vengono specificati nel file% windir% \\ system32 \\ restore \\Filelist.xml. Per altre informazioni, vedere [estensioni di file monitorate](monitored-file-extensions.md).

 

 




