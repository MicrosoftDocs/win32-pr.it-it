---
title: Usare gli handle di contesto per mantenere lo stato nel server
description: Usare gli handle di contesto per mantenere lo stato nel server
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221489"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a>Usare gli handle di contesto per mantenere lo stato nel server

**Procedura consigliata:** Ogni volta che lo stato viene mantenuto nel server tra le chiamate, utilizzare gli handle del contesto.

Gli handle di contesto sono spesso intimidatori per i nuovi programmatori RPC e l'overhead degli handle del contesto di apprendimento potrebbe non essere inizialmente degno di sforzo. Vale la pena perché gli handle di contesto hanno soluzioni predefinite per molti problemi comuni riscontrati nella programmazione di rete che altrimenti sarebbe necessario implementare da zero. Informazioni sugli handle di contesto pagano i dividendi in un secondo momento.

 

 




