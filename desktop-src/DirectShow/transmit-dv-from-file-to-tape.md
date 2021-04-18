---
description: Trasmettere DV da un file a un nastro
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Trasmettere DV da un file a un nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316291"
---
# <a name="transmit-dv-from-file-to-tape"></a>Trasmettere DV da un file a un nastro

La trasmissione dal file DV AVI al nastro VTR è piuttosto complicata dal fatto che i file possono digitare-1 o digitare-2. Per trasmettere un file DV su nastro, eseguire le operazioni seguenti:

1.  Creare un'istanza del filtro del [driver Msdv](msdv-driver.md) . Per altre informazioni, vedere [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).
2.  Verificare che il dispositivo sia in modalità VTR. In caso contrario, non sarà possibile trasmettere su nastro. Vedere [modalità dispositivo](device-mode.md).
3.  Inizializzare il generatore di grafici di acquisizione, come descritto in [informazioni sul generatore di grafici di acquisizione](about-the-capture-graph-builder.md).
4.  Compilare il grafo. La configurazione del grafico dipende dal tipo di file DV:
    -   [Trasmissione da un file di tipo 1](transmit-from-type-1-file.md)
    -   [Trasmissione da un file di tipo 2](transmit-from-type-2-file.md)
5.  Impostare il dispositivo in modalità di sospensione dei record, come descritto in [controllo di una videocamera DV](controlling-a-dv-camcorder.md).
6.  Sospendere il grafico del filtro. Mentre il grafico a filtro è sospeso, invia un flusso continuo che ripete il primo frame di video.
7.  Per avviare la trasmissione, impostare il dispositivo in modalità registrazione e quindi eseguire il grafico del filtro. Il dispositivo richiede una certa quantità di tempo fino a quando l'Head di registrazione non è in grado di registrare, quindi attendere circa due secondi prima di eseguire il grafo. Questo potrebbe comportare alcuni frame duplicati all'inizio del nastro, ma garantisce che non si verifichino perdite di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



