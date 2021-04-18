---
description: Poiché gli elementi duplicati sono i descrittori di socket e non i socket sottostanti, tutti gli Stati associati a un socket vengono mantenuti in comune in tutti i descrittori.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Più handle per un singolo socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306928"
---
# <a name="multiple-handles-to-a-single-socket"></a>Più handle per un singolo socket

Poiché gli elementi duplicati sono i descrittori di socket e non i socket sottostanti, tutti gli Stati associati a un socket vengono mantenuti in comune in tutti i descrittori. Ad esempio, un'operazione [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) eseguita usando un descrittore è successivamente visibile usando un [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) da uno o tutti i descrittori.

La notifica sui socket condivisi è soggetta ai vincoli usuali di [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). Quando si esegue una di queste chiamate utilizzando uno dei descrittori condivisi, viene annullata la registrazione di eventi precedente per il socket, indipendentemente dal descrittore utilizzato per effettuare la registrazione. Quindi, ad esempio, non sarebbe possibile avere un processo di ricezione di eventi di \_ lettura FD ed elaborare B ricevere \_ eventi di scrittura FD. Per le situazioni in cui è necessario un coordinamento rigoroso, è consigliabile che gli sviluppatori utilizzino i thread anziché processi distinti.

 

 
