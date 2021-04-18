---
title: Posizionare e spostare i rettangoli video nello spazio di composizione
description: Posizionamento e trasferimento di rettangoli video nello spazio di composizione
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303984"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Posizionare e spostare i rettangoli video nello spazio di composizione

Quando VMR unisce più flussi di input, posiziona ogni flusso all'interno di un rettangolo normalizzato, denominato "spazio di composizione". All'interno dello spazio di composizione, le coordinate (0,0, 0,0) in (1,0, 1,0) formano il rettangolo video visibile. Tutte le coordinate che esulano da questo rettangolo vengono ritagliate.

Un'applicazione può eseguire effetti speciali con lo spostamento, l'allungamento e la compattazione del video da un flusso di input, modificando il rettangolo di destinazione nello spazio di composizione per quel flusso. Se il rettangolo specificato ha dimensioni diverse rispetto al rettangolo del video nativo, il video nativo verrà compattato o allungato per adattarlo. Il rettangolo di destinazione viene specificato chiamando il metodo [**IVMRMixerControl:: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .

Si supponga, ad esempio, che il flusso 0 (che corrisponde al pin 0) contenga il flusso video principale e il flusso 1 (che corrisponde al pin 1) contenga un video secondario. Il flusso 1 può essere posizionato completamente Offscreen specificando un rettangolo normalizzato di {-1.0 f, 0,0 f, 0,0 f, 1.0 f}. Il flusso 1 può quindi essere spostato nell'area visibile modificando il lato sinistro e destro del rettangolo sulle chiamate successive a **SetOutputRect**:



|        |                             |
|--------|-----------------------------|
| Tempo   | Rettangolo                   |
| t + 0  | {-1.0 f, 0,0 f, 0,0 f, 1.0 f} |
| t + 1  | {-0.9 f, 0,0 f, 0,1 f, 1.0 f} |
| t + 2  | {-0.8 f, 0,0 f, 0.2 f, 1.0 f} |
| ...    | ...                         |
| t + 10 | {0,0 f, 0,0 f, 1.0 f, 1.0 f}  |



 

![trasferimento di un flusso video nello spazio di composizione](images/composition-space.png)

Al momento t + 10, il video del flusso 1 è completamente visibile. In questo esempio, la dimensione nativa del flusso 1 è stata mantenuta mentre era in fase di trasferimento. È anche possibile estendere o ridurre il rettangolo per produrre effetti interessanti. È anche possibile capovolgere il video verticalmente, specificando un valore maggiore per la parte superiore della parte inferiore oppure eseguendo il mirroring del video orizzontalmente, specificando un valore maggiore per il lato sinistro rispetto a quello a destra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



