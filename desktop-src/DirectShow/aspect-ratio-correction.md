---
description: Correzione proporzioni
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Correzione proporzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304209"
---
# <a name="aspect-ratio-correction"></a>Correzione proporzioni

Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.

In modalità di combinazione, il VMR ridimensiona il video con le proporzioni corrette. (Eccezione: vedere [combinazione non quadrata](non-square-mixing.md)). Questa operazione può richiedere l'allungamento del video se le proporzioni preferite non corrispondono alle proporzioni fisiche dell'immagine. Il formato video digitale (DV), ad esempio, è 720 x 480 pixel (3:2), ma deve essere visualizzato con un rapporto di 4:3.

VMR supporta due comportamenti diversi per la correzione di proporzioni:

-   Regolare la dimensione orizzontale o verticale, in modo che l'immagine venga sempre allungata, mai compattata. Questo è il comportamento predefinito.
-   Regolare le dimensioni orizzontali, ovvero l'estensione o la compattazione del video.

Poiché il secondo comportamento (solo regolazione orizzontale) può comportare la compattazione del video, l'immagine di output potrebbe avere una risoluzione minore. Per questo motivo, è preferibile il primo comportamento. Ad esempio, nel caso di 720 x 480 video alle proporzioni 4:3, il comportamento predefinito produce un'immagine 720 x 550, mentre la regolazione orizzontale produce un'immagine 640 x 480 più piccola.

**VMR-7**: per impostare la preferenza di correzione delle proporzioni, chiamare [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect). Impostare il \_ flag MixerPref ARAdjustXorY per il comportamento predefinito oppure deselezionare questo flag solo per la regolazione orizzontale.

**VMR-9**: per impostare la preferenza di correzione delle proporzioni, chiamare [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs). Impostare il \_ flag MixerPref9 ARAdjustXorY per il comportamento predefinito oppure deselezionare questo flag solo per la regolazione orizzontale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



