---
title: Impostazioni acquisizione video
description: Impostazioni acquisizione video
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297895"
---
# <a name="video-capture-settings"></a>Impostazioni acquisizione video

La struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contiene i parametri di controllo per l'acquisizione video di streaming. Questa struttura controlla diversi aspetti del processo di acquisizione e consente di eseguire le attività seguenti:

-   Specificare la frequenza dei fotogrammi.
-   Consente di specificare il numero di buffer video allocati.
-   Disabilitare e abilitare l'acquisizione audio.
-   Specificare l'intervallo di tempo per l'acquisizione.
-   Specificare se durante l'acquisizione viene usato un dispositivo MCI (VCR o videodisco).
-   Consente di specificare il controllo della tastiera o del mouse per lo streaming finale.
-   Consente di specificare il tipo di media video applicato durante l'acquisizione.

È possibile recuperare le impostazioni di acquisizione correnti all'interno della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) inviando il messaggio di [**\_ \_ \_ \_ configurazione della sequenza WM CAP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) a una finestra di acquisizione. È possibile impostare una o più impostazioni di acquisizione correnti aggiornando i membri appropriati della struttura **CAPTUREPARMS** e quindi inviando il messaggio di [**\_ \_ \_ \_ installazione sequenza di WM Cap**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) e **CAPTUREPARMS** a una finestra di acquisizione.

 

 




