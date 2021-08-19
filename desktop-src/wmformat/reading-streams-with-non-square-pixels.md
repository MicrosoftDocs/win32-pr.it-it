---
title: Lettura Flussi con pixel non quadrati
description: Lettura Flussi con pixel non quadrati
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows MEDIA Format SDK, lettura di flussi video
- Windows MEDIA Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows Media Format SDK,pixel (non quadrati)
- Advanced Systems Format (ASF), lettura di flussi video
- ASF (Advanced Systems Format), lettura di flussi video
- Advanced Systems Format (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Advanced Systems Format (ASF), pixel non quadrati
- ASF (Advanced Systems Format), pixel non quadrati
- Advanced Systems Format (ASF), pixel (non quadrati)
- ASF (Advanced Systems Format),pixel (non quadrati)
- lettura di flussi video
- flussi video, lettura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9173c7b5dca81f11a6e35afafe30efa33d86c604adcadb59a51b17ab8130422c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846028"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lettura Flussi con pixel non quadrati

Le applicazioni lettore che devono gestire correttamente i pixel non quadrati devono esaminare sia gli attributi a livello di flusso nell'intestazione ASF che le estensioni dell'unità dati in ogni esempio. Esistono due casi in cui il rettangolo di output deve essere regolato per compensare i pixel non quadrati.

Quando il contenuto di origine è stato acquisito da un dispositivo, ad esempio una fotocamera DV (digital video) con pixel non quadrati nel CCD, un'applicazione di lettura deve regolare il rettangolo di output video in modo che l'immagine venga visualizzata correttamente su un monitor del computer con pixel quadrati.

Quando l'applicazione lettore restituisce un video che verrà riprodotto su una tv NTSC, ad esempio tramite una connessione di uscita S-Video sulla scheda video, è necessario regolare il rettangolo video in modo che l'immagine venga visualizzata correttamente sui pixel non quadrati del programma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per leggere e scrivere video Flussi con pixel non quadrati**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




