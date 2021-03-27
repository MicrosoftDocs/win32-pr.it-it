---
description: L'animazione della tavolozza è una tecnica per simulare il movimento modificando rapidamente i colori delle voci selezionate in una tavolozza dei colori.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animazione tavolozza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754338"
---
# <a name="palette-animation"></a>Animazione tavolozza

L'animazione della tavolozza è una tecnica per simulare il movimento modificando rapidamente i colori delle voci selezionate in una tavolozza dei colori. Un'applicazione può eseguire l'animazione della tavolozza creando una tavolozza logica che contiene voci "riservate" e quindi utilizzando la funzione [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) per modificare i colori in tali voci riservate.

Un'applicazione crea una voce riservata in una tavolozza logica impostando il membro **peFlags** della struttura [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) sul \_ flag riservato PC. Una volta selezionata e realizzata questa tavolozza logica, l'applicazione può chiamare la funzione [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) per modificare una o più voci riservate. Se la tavolozza specificata è associata alla finestra attiva, il sistema aggiorna immediatamente i colori sullo schermo.

 

 
