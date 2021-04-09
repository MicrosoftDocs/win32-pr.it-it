---
title: Configurazione compressore e decompressore
description: Configurazione compressore e decompressore
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Gestione compressione video (VCM), configurazione di compressatori
- VCM (Gestione compressione video), configurazione dei commediatori
- Messaggio ICM_CONFIGURE
- ICQueryConfigure (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955396"
---
# <a name="compressor-and-decompressor-configuration"></a>Configurazione compressore e decompressore

L'applicazione può configurare il compressore o il decompressore automaticamente oppure può consentire all'utente di configurarli. Se è pratico, consentire all'utente di configurare il compressore o il decompressore; in questo modo si evita di considerare tutte le opzioni per il compressore o il decompressore.

L'utente può configurare il compressore o il decompressore usando una finestra di dialogo di configurazione. È possibile inviare il messaggio di [**\_ configurazione ICM**](icm-configure.md) a VCM (oppure usare la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) per determinare se un compressore o un decompressore può visualizzare una finestra di dialogo di configurazione. In tal caso, inviare il \_ messaggio di configurazione ICM (oppure usare la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) per visualizzarlo.

L'applicazione può inviare i messaggi di stato [**MCI \_ GetState**](icm-getstate.md) e [**ICM \_**](icm-setstate.md) (oppure usare le macro [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) per ottenere e impostare lo stato di un compressore o un decompressore. Se l'applicazione crea o modifica lo stato, deve ottenere il layout dei dati del compressore o del decompressore prima di ripristinarne lo stato. In alternativa, se l'applicazione ottiene lo stato da un compressore o da un decompressore e lo usa per ripristinare lo stato in una sessione successiva, deve assicurarsi che ripristini solo le informazioni sullo stato ottenute dal compressore o dal decompressore attualmente in uso.

 

 




