---
description: Acquisisci DV in file
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Acquisisci DV in file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d886b964502d705f5902c17de8e6e008a11a31699de40b3089033867873fa021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814341"
---
# <a name="capture-dv-to-file"></a>Acquisisci DV in file

Questa sezione descrive come acquisire video digitali (DV) da una fotocamera DV o da un nastro VTR.

1.  Creare un'istanza del [filtro del driver MSDV.](msdv-driver.md) Per altre informazioni, vedere [Selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).
2.  Inizializzare capture Graph Builder, come descritto in [About the Capture Graph Builder](about-the-capture-graph-builder.md).
3.  Compilare il grafico di acquisizione, a seconda del tipo di file di destinazione:
    -   [Acquisire un file DV di tipo 1](capture-a-type-1-dv-file.md)
    -   [Acquisire un file DV di tipo 2](capture-a-type-2-dv-file.md)
    -   [Acquisisci DV in RGB non compresso](capture-dv-to-uncompressed-rgb.md)
4.  Eseguire il grafo.

L'acquisizione da un nastro VTR funziona esattamente come l'acquisizione di video live dalla fotocamera, con la differenza che è necessario riprodurre il nastro, come descritto in Controllo di un [camcorder DV.](controlling-a-dv-camcorder.md) Per evitare la perdita di fotogrammi, eseguire prima il grafo e quindi riprodurre il nastro. Al termine della trasmissione, arrestare prima il nastro e quindi arrestare il grafo.

> [!Note]  
> Il camcorder deve essere in modalità VTR. Vedere [Modalità dispositivo](device-mode.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[File AVI DV type-1 e Type-2](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



