---
title: Accesso e controllo dei dati del frame DWM
description: In questo argomento vengono illustrate le API di Gestione finestre desktop (DWM) utilizzate per la pianificazione e la presentazione multimediale.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- API di presentazione Gestione finestre desktop (DWM), pianificazione e supporti
- DWM (Gestione finestre desktop), pianificazione e API presentazione di supporti
- API per la pianificazione e la presentazione multimediale
- Gestione finestre desktop (DWM), accesso ai dati del frame
- DWM (Gestione finestre desktop), accesso ai dati del frame
- accesso ai dati del frame
- Gestione finestre desktop (DWM), controllo dei dati del frame
- DWM (Gestione finestre desktop), controllo dei dati del frame
- controllo dei dati del frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330279"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>Accesso e controllo dei dati del frame DWM

In questo argomento vengono illustrate le API di Gestione finestre desktop (DWM) utilizzate per la pianificazione e la presentazione multimediale.

## <a name="dwm-frame-timing-api"></a>API intervallo frame DWM

Le API per la pianificazione e la presentazione multimediale consentono un controllo più dettagliato del momento in cui l'immagine desktop viene composita e presentata. Questa operazione è in genere necessaria per le applicazioni per la riproduzione di file multimediali e video per le quali DWM viene eseguito in modo asincrono con la propria pianificazione di presentazione, che può generare artefatti di campionamento, se non strettamente controllati.

Le funzioni di pianificazione e presentazione multimediale includono quanto segue. I dettagli relativi all'utilizzo sono disponibili in tali pagine.

-   [**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss). Notifica a DWM di abilitare la pianificazione MMCSS (Multimedia Class Schedule Service) mentre il processo chiamante è attivo.
-   [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo). Recupera le informazioni sulla tempistica di composizione corrente.
-   [**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration). Modifica il numero di aggiornamenti durante i quali verrà visualizzato il frame precedente.
-   [**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration). Imposta il numero di aggiornamenti in cui visualizzare il frame presentato.
-   [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters). Imposta i parametri presenti per la composizione del frame.

 

 




