---
description: Uso della decimazione per ottimizzare le prestazioni di combinazione
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Uso della decimazione per ottimizzare le prestazioni di combinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883102"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Uso della decimazione per ottimizzare le prestazioni di combinazione

> [!IMPORTANT]
> L'ottimizzazione descritta in questa sezione dipende molto dall'hardware sottostante. A meno che non sia possibile garantire il tipo di hardware grafico che verrà usato con l'applicazione, l'aspetto dell'immagine video potrebbe risultare grave.

 

Per HDTV è necessaria una quantità elevata di potenza di elaborazione, che nei sistemi più recenti viene fornita principalmente dalla scheda grafica. Tuttavia, anche se la scheda grafica e il decodificatore sono in grado di supportare le risoluzioni di 1920x1080, è possibile che l'utente non abbia sempre il proprio monitor impostato su questa risoluzione. In questo caso, il chip grafico è necessario per creare un'immagine 1920 x 1080, quindi ridurre la risoluzione prima di inviarla al buffer dei frame.

Poiché si tratta di una perdita di potenza di elaborazione, VMR offre un modo per decimare (ridurre) l'immagine nel momento in cui viene eseguito il rendering sulla superficie di DirectDraw. In questo modo si elimina la copia di memoria aggiuntiva necessaria se l'immagine deve essere ridimensionata dopo il rendering.

**VMR-7:** Per abilitare la decimazione, chiamare [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con il \_ flag DecimateOutput di MixerPref.

**VMR-9:** Per abilitare la decimazione, chiamare [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il \_ flag DecimateOutput di MixerPref9.

Il metodo **SetMixingPrefs** deve essere chiamato prima della connessione di VMR. I flag di preferenza di combinazione non possono essere modificati dopo l'esecuzione del grafo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



