---
title: Monitoraggio dello stato di avanzamento dei decompressori e dei decompressori
description: Monitoraggio dello stato di avanzamento dei decompressori e dei decompressori
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- gestione compressione video(VCM), monitoraggio
- VCM (Gestione compressione video),monitoraggio
- Funzione ICSetStatusProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44707cb6a8fbdb19b1d71fed6c71498b51936b9d089354277c6767586b4b8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373504"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Monitoraggio dello stato di avanzamento dei decompressori e dei decompressori

L'applicazione può monitorare lo stato di avanzamento di un'operazione di lunga durata eseguita da un dispositivo di decompressione o un'operazione di decompressione inviando l'indirizzo di una funzione di callback. È possibile usare la [**funzione ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) per inviare l'indirizzo al ricevitore o decompressore. Quando l'utente o il decompressore riceve questo indirizzo, invia messaggi di stato alla funzione. Questi messaggi indicano se l'operazione è in corso di avvio, arresto, cede o sta procedendo.

 

 




