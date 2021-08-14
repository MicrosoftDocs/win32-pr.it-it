---
description: Le funzioni di debug possono essere usate per creare un debugger di base basato su eventi.
ms.assetid: 3c9e186b-6844-4126-b035-a3541880e109
title: Informazioni sul debug di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d927deaa4120f52922e22fecc05c9cdf997eaf51355bb830a7ea1065985c593
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984511"
---
# <a name="about-basic-debugging"></a>Informazioni sul debug di base

Le [funzioni di debug](debugging-functions.md) possono essere usate per creare un debugger di base basato su eventi. *Basato su eventi indica* che il debugger viene informato ogni volta che si verificano determinati eventi nel processo sottoposto a debug. La notifica consente al debugger di eseguire l'azione appropriata in risposta agli eventi.

Per una panoramica dei termini di debug, vedere [Terminologia del debug.](debugging-terminology.md)

[Supporto del debug da funzioni di elaborazione, thread](debug-support-from-process-thread-and-exception-functions.md) ed eccezioni descrive le funzionalità specifiche del debug di determinate funzioni di gestione di processi, thread e eccezioni.

[Creazione di un debugger di](creating-a-basic-debugger.md) base descrive l'uso delle funzioni di debug di base per creare un debugger semplice. Queste funzioni consentono a un'applicazione di attendere gli eventi di debug, causare eccezioni del punto di interruzione, trasferire il controllo di esecuzione al debugger e così via.

[Eventi di debug](debugging-events.md) descrive il meccanismo degli eventi di debug. Gli eventi di debug determinano la notifica al debugger da parte del sistema.

 

 



