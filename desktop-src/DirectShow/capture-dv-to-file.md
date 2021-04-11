---
description: Acquisisci DV nel file
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Acquisisci DV nel file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341916"
---
# <a name="capture-dv-to-file"></a>Acquisisci DV nel file

Questa sezione descrive come acquisire video digitali (DV) da una videocamera DV o da un nastro VTR.

1.  Creare un'istanza del filtro del [driver Msdv](msdv-driver.md) . Per altre informazioni, vedere [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).
2.  Inizializzare il generatore di grafici di acquisizione, come descritto in [informazioni sul generatore di grafici di acquisizione](about-the-capture-graph-builder.md).
3.  Compilare il grafico di acquisizione, a seconda del tipo di file di destinazione:
    -   [Acquisire un file DV di tipo 1](capture-a-type-1-dv-file.md)
    -   [Acquisire un file DV di tipo 2](capture-a-type-2-dv-file.md)
    -   [Acquisisci DV in RGB non compresso](capture-dv-to-uncompressed-rgb.md)
4.  Eseguire il grafo.

L'acquisizione da un nastro VTR funziona esattamente come l'acquisizione di video live dalla fotocamera, ad eccezione del fatto che è necessario riprodurre il nastro, come descritto in [controllo di una videocamera DV](controlling-a-dv-camcorder.md). Per evitare la perdita di frame, eseguire prima il grafo, quindi riprodurre il nastro. Al termine della trasmissione, arrestare prima il nastro e quindi arrestare il grafo.

> [!Note]  
> La videocamera deve essere in modalità VTR. Vedere [modalità dispositivo](device-mode.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Tipo-1 e file AVI DV di tipo 2](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



