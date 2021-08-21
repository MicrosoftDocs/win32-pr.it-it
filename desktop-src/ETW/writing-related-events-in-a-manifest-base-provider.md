---
description: Usare la funzione EventWriteTransfer quando diversi componenti vogliono correlare i propri eventi in uno scenario di traccia end-to-end.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Scrittura di eventi correlati in un provider basato su manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f6d09e7e95617b662c3530497b199925921ef9abfd4f3825a5ac799886f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015209"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Scrittura di eventi correlati in un provider basato su manifesto

Usare la [**funzione EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) quando diversi componenti vogliono correlare i propri eventi in uno scenario di traccia end-to-end. Ad esempio, i componenti A, B e C eseguono operazioni su un'attività correlata e vogliono collegare tutti gli eventi correlati a tale attività.

ETW usa l'archiviazione locale di thread per rendere disponibile l'identificatore di attività del componente precedente al componente successivo. Il componente recupera l'identificatore del componente precedente dalla risorsa di archiviazione locale e imposta l'identificatore di attività correlato su di esso. Il consumer può quindi usare l'identificatore di attività correlato per eseguire la catena degli eventi da un componente a quello successivo.

 

 



