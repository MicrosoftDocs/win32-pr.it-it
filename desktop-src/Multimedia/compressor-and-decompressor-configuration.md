---
title: Configurazione del compressore e del decompressore
description: Configurazione del compressore e del decompressore
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- gestione compressione video(VCM), configurazione di compresse
- VCM (gestione compressione video), configurazione di compresse
- ICM_CONFIGURE messaggio
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8905ea35d65fc3eda3ddee130039503d8e26555665aae9efa517cb399349475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144976"
---
# <a name="compressor-and-decompressor-configuration"></a>Configurazione del compressore e del decompressore

L'applicazione può configurare automaticamente il compressore o il decompressore oppure può consentire all'utente di configurarli. Se è pratico, consentire all'utente di configurare il compressore o il decompressore; in modo da non considerare tutte le opzioni per il decompressore o il compressore.

L'utente può configurare il compressore o il decompressore usando una finestra di dialogo di configurazione. È possibile inviare il messaggio [**ICM \_ CONFIGURE**](icm-configure.md) a VCM (o usare la macro [**ICQueryConfigure)**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) per determinare se un compilatore o un decompressore può visualizzare una finestra di dialogo di configurazione. In tal caso, inviare ICM messaggio CONFIGURE (o usare \_ la macro [**ICConfigure)**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) per visualizzarlo.

L'applicazione può inviare i messaggi [**ICM \_ GETSTATE**](icm-getstate.md) e [**\_ setSTATE di ICM**](icm-setstate.md) (oppure usare le macro [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)e [**ICSetState)**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) per ottenere e impostare lo stato di un dispositivo di compressione o decompressione. Se l'applicazione crea o modifica lo stato, deve ottenere il layout dei dati di compressione o decompressione prima di ripristinarne lo stato. In alternativa, se l'applicazione ottiene lo stato da un compressore o da un decompressore e lo usa per ripristinare lo stato in una sessione successiva, deve assicurarsi che ripristini solo le informazioni sullo stato ottenute dal compressore o dal decompressore attualmente in uso.

 

 




