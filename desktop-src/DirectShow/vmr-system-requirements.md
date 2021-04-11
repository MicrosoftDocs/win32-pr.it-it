---
description: Requisiti di sistema di VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Requisiti di sistema di VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232279"
---
# <a name="vmr-system-requirements"></a>Requisiti di sistema di VMR

VMR usa esclusivamente le funzionalità di elaborazione grafica della scheda video del computer; il VMR non esegue alcuna operazione di fusione o rendering dei video usando il processore host, perché a tale scopo potrebbe avere un notevole effetto sulla frequenza dei fotogrammi e sulla qualità del video visualizzato. Quando si sfruttano le nuove funzionalità offerte da VMR, in particolare la fusione di più flussi video e/o immagini di applicazioni, le prestazioni complessive ottenute dipendono fortemente dalle funzionalità della scheda grafica utilizzata nel computer. Le schede grafiche che offrono prestazioni ottimali con VMR hanno il seguente supporto hardware integrato:

-   Supporto per le superfici di trama Direct3D e "non di potenza di 2".
-   Possibilità di StretchBlt da YUV a superfici DirectDraw RGB.
-   Almeno 16 MB di memoria video se è necessario combinare più flussi video. La quantità effettiva di memoria necessaria dipende dalle dimensioni dell'immagine dei flussi video e dalla risoluzione della modalità di visualizzazione usata.
-   Supporto per una sovrapposizione RGB o la possibilità di fondersi a una superficie di sovrimpressione YUV.
-   Video con accelerazione hardware (supporto per l'accelerazione video DirectX) con decodifica.
-   Velocità di riempimento in pixel elevate.

> [!Note]  
> Il VMR richiede che il monitor di sistema sia impostato per una profondità di colore di almeno 16 bit. Il VMR non può essere impostato su uno stato di esecuzione se il monitoraggio è impostato per 256 colori. Inoltre, alcune schede video non possono eseguire operazioni Direct3D quando la visualizzazione è impostata su 24 bit per pixel.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering del mixaggio video](about-the-video-mixing-render.md)
</dt> </dl>

 

 



