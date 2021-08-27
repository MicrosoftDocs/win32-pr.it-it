---
description: Trasmettere DV da file a nastro
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Trasmettere DV da file a nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bcd7bf716466cda2fc23a03968da4a51c005070f885183390f944d14994ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086791"
---
# <a name="transmit-dv-from-file-to-tape"></a>Trasmettere DV da file a nastro

La trasmissione dal file AVI DV al nastro VTR è piuttosto complessa dal fatto che i file possono digitare-1 o tipo-2. Per trasmettere un file DV su nastro, eseguire le operazioni seguenti:

1.  Creare un'istanza del [filtro del driver MSDV.](msdv-driver.md) Per altre informazioni, vedere [Selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).
2.  Assicurarsi che il dispositivo sia in modalità VTR. In caso contrario, non è possibile trasmettere su nastro. Vedere [Modalità dispositivo](device-mode.md).
3.  Inizializzare capture Graph Builder, come descritto in [About the Capture Graph Builder](about-the-capture-graph-builder.md).
4.  Compilare il grafo. La configurazione del grafo dipende dal tipo di file DV:
    -   [Trasmettere dal file di tipo 1](transmit-from-type-1-file.md)
    -   [Trasmettere dal file di tipo 2](transmit-from-type-2-file.md)
5.  Mettere il dispositivo in modalità di sospensione record, come descritto in [Controllo di un camcorder DV.](controlling-a-dv-camcorder.md)
6.  Sospendere il grafico dei filtri. Mentre il grafico dei filtri è sospeso, invia un flusso continuo che ripete il primo fotogramma del video.
7.  Per avviare la trasmissione, impostare il dispositivo in modalità di registrazione e quindi eseguire il grafico dei filtri. Il dispositivo richiede una certa quantità di tempo fino a quando la testina di registrazione non è in grado di registrare, quindi attendere circa due secondi prima di eseguire il grafico. Ciò potrebbe comportare alcuni fotogrammi duplicati all'inizio del nastro, ma garantisce che non venga perso alcun dato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



