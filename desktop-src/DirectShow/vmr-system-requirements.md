---
description: Requisiti di sistema di VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Requisiti di sistema di VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d03d5a195f675b911dff85860592c3ec3b5a39ec4f65a51cdc594bc8744906
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633001"
---
# <a name="vmr-system-requirements"></a>Requisiti di sistema di VMR

La macchina virtuale usa esclusivamente le funzionalità di elaborazione grafica della scheda video del computer. la macchina virtuale non esegue alcuna fusione o rendering del video usando il processore host, perché a tale scopo influisce notevolmente sulla frequenza dei fotogrammi e sulla qualità del video visualizzato. Quando si sfruttano le nuove funzionalità offerte dalla macchina virtuale, in particolare la fusione di più flussi video e/o immagini dell'applicazione, le prestazioni complessive ottenute dipendono fortemente dalle funzionalità della scheda grafica usata nel computer. Le schede grafiche che hanno prestazioni con la macchina virtuale dispongono del supporto hardware seguente:

-   Supporto per yuv e superfici di trama Direct3D "non potenza di 2".
-   Possibilità di stretchblt dalle superfici YUV a RGB DirectDraw.
-   Almeno 16 MB di memoria video se più flussi video devono essere uniti insieme. La quantità effettiva di memoria necessaria dipende dalle dimensioni dell'immagine dei flussi video e dalla risoluzione della modalità di visualizzazione usata.
-   Supporto per una sovrimpressione RGB o la possibilità di eseguire la fusione con una superficie di sovrapposizione YUV.
-   Decodifica video con accelerazione hardware (supporto per l'accelerazione video DirectX).
-   Frequenze di riempimento pixel elevate.

> [!Note]  
> La macchina virtuale richiede che il monitor di sistema sia impostato per una profondità di colore di almeno 16 bit. La macchina virtuale non può essere impostata in uno stato di esecuzione se il monitoraggio è impostato su 256 colori. Inoltre, alcune schede video non possono eseguire operazioni Direct3D quando la visualizzazione è impostata su 24 bit per pixel.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul rendering di combinazione di video](about-the-video-mixing-render.md)
</dt> </dl>

 

 



