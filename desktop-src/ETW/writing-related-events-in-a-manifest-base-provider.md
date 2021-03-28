---
description: Utilizzare la funzione EventWriteTransfer quando più componenti desiderano correlare gli eventi in uno scenario di traccia end-to-end.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Scrittura di eventi correlati in un provider basato su manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527282"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Scrittura di eventi correlati in un provider basato su manifesto

Utilizzare la funzione [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) quando più componenti desiderano correlare gli eventi in uno scenario di traccia end-to-end. I componenti A, B e C, ad esempio, eseguono operazioni su un'attività correlata e vogliono collegare tutti gli eventi correlati a tale attività.

ETW usa l'archiviazione locale di thread per rendere disponibile l'identificatore di attività del componente precedente al componente successivo. Il componente recupera l'identificatore del componente precedente dalla risorsa di archiviazione locale e ne imposta l'identificatore di attività correlato. Il consumer può quindi utilizzare l'identificatore di attività correlato per scorrere la catena degli eventi da un componente a quello successivo.

 

 



