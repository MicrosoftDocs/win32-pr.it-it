---
title: Acquisizione video Impostazioni
description: Acquisizione video Impostazioni
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Struttura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50eb26170c8b1594d288cec903ef0c05867a24db2d5a89a6ad60f66eef4fd0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135589"
---
# <a name="video-capture-settings"></a>Acquisizione video Impostazioni

La [**struttura CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contiene i parametri di controllo per l'acquisizione di video in streaming. Questa struttura controlla diversi aspetti del processo di acquisizione e consente di eseguire le attività seguenti:

-   Specificare la frequenza dei fotogrammi.
-   Specificare il numero di buffer video allocati.
-   Disabilitare e abilitare l'acquisizione audio.
-   Specificare l'intervallo di tempo per l'acquisizione.
-   Specificare se durante l'acquisizione viene usato un dispositivo MCI (vcr o videodisc).
-   Specificare la tastiera o il controllo del mouse per terminare lo streaming.
-   Specificare il tipo di media video applicata durante l'acquisizione.

È possibile recuperare le impostazioni di acquisizione correnti all'interno della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) inviando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) a una finestra di acquisizione. È possibile impostare una o più impostazioni di acquisizione correnti aggiornando i membri appropriati della struttura **CAPTUREPARMS** e quindi inviando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) e **CAPTUREPARMS** a una finestra di acquisizione.

 

 




