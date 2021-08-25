---
title: Regolazione di velocità, volume e zoom
description: Regolazione di velocità, volume e zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Macro MCIWndSetSpeed
- Macro MCIWndGetSpeed
- Macro MCIWndSetVolume
- Macro MCIWndGetVolume
- Macro MCIWndSetZoom
- Macro MCIWndGetZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed63549683a92d457b9b91ac967ff9098235bf8d9cbd60b1ea332624886d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808571"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Regolazione di velocità, volume e zoom

Le macro di velocità, volume e zoom forniscono la  funzionalità dei comandi **Visualizza,** **Volume** e Velocità del menu MCIWnd. Le macro descritte in questa sezione vengono in genere usate con video e altri dispositivi che visualizzano immagini durante la riproduzione.

Alcuni dispositivi supportano più cambi di velocità di riproduzione. È possibile impostare la velocità di riproduzione per questi dispositivi usando la macro [**MCIWndSetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) Questa macro definisce la velocità di riproduzione come 1000. Valori più elevati indicano velocità più elevate. I valori più bassi indicano velocità più lente.

È possibile recuperare la velocità di riproduzione corrente usando la macro [**MCIWndGetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) Questa macro usa gli stessi valori e gli stessi intervalli usati da **MCIWndSetSpeed.**

Alcuni dispositivi supportano le modifiche al volume. È possibile regolare o impostare il volume usando la macro [**MCIWndSetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) Questa macro definisce il livello di volume normale come 1000. I valori più alti indicano volumi più alti. I valori inferiori indicano volumi più silenziosi.

È possibile recuperare il livello del volume corrente usando la macro [**MCIWndGetVolume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) Questa macro usa gli stessi valori numerici e gli stessi intervalli usati da **MCIWndSetVolume.**

Per i dispositivi che usano una finestra di riproduzione, MCIWnd supporta una funzionalità di zoom che imposta le dimensioni dell'immagine di riproduzione. È possibile impostare le dimensioni dell'immagine di riproduzione usando la macro [**MCIWndSetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) La macro ridefinisce le dimensioni dell'immagine di riproduzione mantenendo proporzioni costanti per l'immagine. Il valore di zoom è definito come percentuale delle dimensioni dell'immagine originale. Pertanto, 100 rappresenta le dimensioni originali dell'immagine, 50 indica che l'immagine mostrata è la metà delle dimensioni originali e 200 indica che l'immagine mostrata è il doppio delle dimensioni originali.

È possibile recuperare il valore di zoom corrente usando la macro [**MCIWndGetZoom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) Questa macro usa gli stessi valori e gli stessi intervalli usati da **MCIWndSetZoom.**

> [!Note]  
> I driver audio e audio waveform-audio MCI CD standard non supportano le variazioni di volume o velocità.

 

 

 




