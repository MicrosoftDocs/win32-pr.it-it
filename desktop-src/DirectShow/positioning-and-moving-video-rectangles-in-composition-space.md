---
title: Posizionare e spostare rettangoli video nello spazio di composizione
description: Posizionamento e spostamento di rettangoli video nello spazio di composizione
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909629"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Posizionare e spostare rettangoli video nello spazio di composizione

Quando vmR combina più flussi di input, posiziona ogni flusso all'interno di un rettangolo normalizzato, denominato "spazio di composizione". All'interno dello spazio di composizione, le coordinate da 0,0, 0,0 a (1,0, 1,0) formano il rettangolo video visibile. Tutte le coordinate esterne a questo rettangolo vengono ritagliate.

Un'applicazione può eseguire effetti speciali con lo spostamento, l'estensione e la riduzione del video da un flusso di input, modificando il rettangolo di destinazione nello spazio di composizione per tale flusso. Se le dimensioni del rettangolo specificato sono diverse da quelle del rettangolo video nativo, il video nativo verrà ridotto o adattato. Il rettangolo di destinazione viene specificato chiamando il [**metodo IVMRMixerControl::SetOutputRect.**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs)

Si supponga, ad esempio, che il flusso 0 (che corrisponde al pin 0) contenga il flusso video principale e che il flusso 1 (che corrisponde al pin 1) contenga un video secondario. Il flusso 1 può essere posizionato completamente fuori schermo specificando un rettangolo normalizzato di { -1.0f, 0.0f, 0.0f, 1.0f }. Il flusso 1 può quindi essere spostato nell'area visibile modificando i lati sinistro e destro del rettangolo nelle chiamate successive a **SetOutputRect:**



| Label | Valore |
|--------|-----------------------------|
| Tempo   | Rettangolo                   |
| t + 0  | { -1.0f, 0.0f, 0.0f, 1.0f } |
| t + 1  | { -0.9f, 0.0f, 0.1f, 1.0f } |
| t + 2  | { -0.8f, 0.0f, 0.2f, 1.0f } |
| ...    | ...                         |
| t + 10 | { 0.0f, 0.0f, 1.0f, 1.0f }  |



 

![spostamento di un flusso video nello spazio di composizione](images/composition-space.png)

Al momento t+10, il video dal flusso 1 è completamente visibile. In questo esempio sono stati mantenute le dimensioni native del flusso 1 durante lo spostamento. È anche possibile estendere o ridurre il rettangolo per produrre effetti interessanti. È anche possibile capovolgere il video verticalmente, specificando un valore maggiore per la parte superiore rispetto alla parte inferiore o rispecchiando il video orizzontalmente, specificando un valore maggiore per la parte sinistra rispetto a destra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione vmr](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



