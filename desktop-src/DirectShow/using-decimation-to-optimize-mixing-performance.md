---
description: Uso di Contrasto per ottimizzare la combinazione di prestazioni
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Uso di Contrasto per ottimizzare la combinazione di prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2218566ab31d159f6d0ab74320aa45eb5780bdc3de151de8a7c642016441bacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049620"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>Uso di Contrasto per ottimizzare la combinazione di prestazioni

> [!IMPORTANT]
> L'ottimizzazione descritta in questa sezione dipende in modo molto dipendente dall'hardware sottostante. A meno che non sia possibile garantire quale tipo di hardware grafico verrà usato con l'applicazione, l'aspetto dell'immagine video potrebbe peggiorare in modo grave.

 

HDTV richiede una grande potenza di elaborazione, che nei sistemi più nuovi viene fornita principalmente dalla scheda grafica. Tuttavia, anche se la scheda grafica e il decodificatore possono supportare risoluzioni di 1920x1080, è possibile che il monitor dell'utente non sia sempre impostato su questa risoluzione. In questo caso, il chip grafico è necessario per creare un'immagine 1920 x 1080 e quindi ridurre la risoluzione prima di inviarla al buffer dei frame.

Poiché si tratta di uno spreco di potenza di elaborazione, la macchina virtuale offre un modo per ridurre l'immagine nel momento in cui viene eseguito il rendering sulla superficie DirectDraw. In questo modo si elimina la copia di memoria aggiuntiva necessaria se l'immagine deve essere ridimensionata dopo il rendering.

**VMR-7:** Per abilitare l'ingrandimento, chiamare [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con il flag MixerPref \_ BlocchiteOutput.

**VMR-9:** Per abilitare la propagazione, chiamare [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il flag MixerPref9 \_ IngrandimentoteOutput.

Il **metodo SetMixingPrefs** deve essere chiamato prima che la macchina virtuale sia connessa. I flag di preferenza di combinazione non possono essere modificati quando il grafico è in esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



