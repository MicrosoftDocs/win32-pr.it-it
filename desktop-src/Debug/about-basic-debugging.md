---
description: Le funzioni di debug possono essere utilizzate per creare un debugger di base basato su eventi.
ms.assetid: 3c9e186b-6844-4126-b035-a3541880e109
title: Informazioni sul debug di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa3e2889d860d747978f2e8866094b0f866910c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877465"
---
# <a name="about-basic-debugging"></a>Informazioni sul debug di base

Le [funzioni di debug](debugging-functions.md) possono essere utilizzate per creare un debugger di base basato su eventi. La guida basata sugli *eventi* indica che il debugger riceve una notifica ogni volta che si verificano determinati eventi nel processo di cui è in corso il debug. La notifica consente al debugger di eseguire l'azione appropriata in risposta agli eventi.

Per una panoramica dei termini di debug, vedere [terminologia di debug](debugging-terminology.md).

Il [supporto del debug da funzioni di processo, thread e di eccezione](debug-support-from-process-thread-and-exception-functions.md) descrive le funzionalità specifiche del debug di determinate funzioni di elaborazione, thread e gestione delle eccezioni.

La [creazione di un debugger di base](creating-a-basic-debugger.md) descrive l'utilizzo delle funzioni di debug di base per creare un debugger semplice. Queste funzioni consentono a un'applicazione di attendere gli eventi di debug, causare eccezioni del punto di interruzione, trasferire il controllo di esecuzione al debugger e così via.

[Gli eventi di debug](debugging-events.md) descrivono il meccanismo dell'evento di debug. Gli eventi di debug fanno sì che il sistema invii una notifica al debugger.

 

 



