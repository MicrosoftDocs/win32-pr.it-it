---
description: Poiché i duplicati sono i descrittori socket e non i socket sottostanti, tutti gli stati associati a un socket sono mantenuti in comune tra tutti i descrittori.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Più handle per un singolo socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e402d19c3306158a905f2e9ddc263649e52d214a3d9441509e7a277f7d2800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121401"
---
# <a name="multiple-handles-to-a-single-socket"></a>Più handle per un singolo socket

Poiché i duplicati sono i descrittori socket e non i socket sottostanti, tutti gli stati associati a un socket sono mantenuti in comune tra tutti i descrittori. Ad esempio, [**un'operazione WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) eseguita usando un descrittore è successivamente visibile usando [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) da uno o tutti i descrittori.

La notifica sui socket condivisi è soggetta ai soliti vincoli [**di WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). L'emissione di una di queste chiamate usando uno dei descrittori condivisi annulla qualsiasi registrazione dell'evento precedente per il socket, indipendentemente dal descrittore usato per effettuare tale registrazione. Pertanto, ad esempio, non sarebbe possibile che il processo A riceva eventi FD READ e che \_ il processo B riceva eventi FD \_ WRITE. In situazioni in cui è necessario un coordinamento così stretto, è consigliabile che gli sviluppatori considerino l'uso di thread anziché di processi separati.

 

 
