---
title: Monitoraggio dello stato di compressione e decompressione
description: Monitoraggio dello stato di compressione e decompressione
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Gestione compressione video (VCM), monitoraggio
- VCM (Video Compression Manager), monitoraggio
- ICSetStatusProc (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298355"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Monitoraggio dello stato di compressione e decompressione

L'applicazione può monitorare lo stato di avanzamento di un'operazione di lunga durata eseguita da un compressore o da un decompressore inviando l'indirizzo di una funzione di callback. È possibile usare la funzione [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) per inviare l'indirizzo al compressore o al decompressore. Quando il compressore o il decompressore riceve questo indirizzo, invia messaggi di stato alla funzione. Questi messaggi indicano se l'operazione viene avviata, arrestata, cedente o prosegue.

 

 




