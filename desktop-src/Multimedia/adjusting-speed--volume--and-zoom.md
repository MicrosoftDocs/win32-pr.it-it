---
title: Regolazione della velocità, del volume e dello zoom
description: Regolazione della velocità, del volume e dello zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed (macro)
- MCIWndGetSpeed (macro)
- MCIWndSetVolume (macro)
- MCIWndGetVolume (macro)
- MCIWndSetZoom (macro)
- MCIWndGetZoom (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396066"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Regolazione della velocità, del volume e dello zoom

Le macro velocità, volume e zoom forniscono le funzionalità dei comandi **Visualizza**, **volume** e **velocità** del menu MCIWnd. Le macro descritte in questa sezione vengono in genere usate con video e altri dispositivi che visualizzano immagini durante la riproduzione.

Alcuni dispositivi supportano più modifiche della velocità di riproduzione. È possibile impostare la velocità di riproduzione per questi dispositivi usando la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) . Questa macro definisce la velocità di riproduzione come 1000. Valori più elevati indicano velocità più veloci. I valori inferiori indicano velocità più lente.

È possibile recuperare la velocità di riproduzione corrente usando la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) . Questa macro USA gli stessi valori e l'intervallo di quelli usati da **MCIWndSetSpeed**.

Alcuni dispositivi supportano le modifiche del volume. È possibile modificare o impostare il volume utilizzando la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) . Questa macro definisce il livello di volume normale come 1000. I valori più alti indicano volumi più potenti. I valori inferiori indicano volumi più tranquilli.

È possibile recuperare il livello del volume corrente usando la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) . Questa macro USA gli stessi valori numerici e gli stessi intervalli di quelli usati da **MCIWndSetVolume**.

Per i dispositivi che usano una finestra di riproduzione, MCIWnd supporta una funzionalità di zoom che consente di impostare le dimensioni dell'immagine di riproduzione. È possibile impostare le dimensioni dell'immagine di riproduzione usando la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) . La macro ridefinisce le dimensioni dell'immagine di riproduzione mantenendo una proporzione costante per l'immagine. Il valore di zoom viene definito come percentuale delle dimensioni originali dell'immagine. Pertanto, 100 rappresenta le dimensioni originali dell'immagine, 50 indica che l'immagine mostrata è la metà delle dimensioni originali e 200 indica che l'immagine mostrata è il doppio delle dimensioni originali.

È possibile recuperare il valore di zoom corrente usando la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) . Questa macro USA gli stessi valori e l'intervallo di quelli usati da **MCIWndSetZoom**.

> [!Note]  
> I driver audio e waveform CD di MCI standard non supportano le modifiche del volume o della velocità.

 

 

 




