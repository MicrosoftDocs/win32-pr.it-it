---
title: Usare handle di contesto per mantenere lo stato nel server
description: Usare handle di contesto per mantenere lo stato nel server
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9360d4edf95c06cef30a0e07f0e541a89823e89b163d5bbb61e0fb686a4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010959"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a>Usare handle di contesto per mantenere lo stato nel server

**Procedura consigliata:** Ogni volta che lo stato viene mantenuto nel server tra le chiamate, usare handle di contesto.

Gli handle di contesto sono spesso in difficoltà per i nuovi programmatori RPC e il sovraccarico degli handle di contesto di apprendimento potrebbe inizialmente non risultare utile. Ne vale la pena perché gli handle di contesto hanno soluzioni incorporate per molti problemi comuni riscontrati nella programmazione di rete che altrimenti sarebbe necessario eseguire da zero. La comprensione degli handle di contesto paga i dividendi in un secondo momento.

 

 




