---
title: Lettura di flussi con pixel non quadrati
description: Lettura di flussi con pixel non quadrati
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media Format SDK, lettura di flussi video
- Windows Media Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows Media Format SDK, pixel (non quadrato)
- Formato di sistemi avanzati (ASF), lettura di flussi video
- ASF (Advanced Systems Format), lettura di flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Formato di sistemi avanzati (ASF), pixel non quadrati
- ASF (formato avanzato dei sistemi), pixel non quadrati
- Formato di sistemi avanzati (ASF), pixel (non quadrato)
- ASF (formato avanzato dei sistemi), pixel (non quadrato)
- lettura di flussi video
- flussi video, lettura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrato)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106299001"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lettura di flussi con pixel non quadrati

Le applicazioni Reader che devono gestire correttamente i pixel non quadrati devono esaminare sia gli attributi a livello di flusso nell'intestazione ASF che le estensioni dell'unità dati in ogni esempio. Esistono due casi in cui è necessario modificare il rettangolo di output per compensare i pixel non quadrati.

Quando il contenuto di origine è stato acquisito da un dispositivo, ad esempio una fotocamera DV (video digitale) con pixel non quadrati nel CCD, un'applicazione Reader deve modificare il relativo rettangolo di output video in modo che l'immagine venga visualizzata correttamente in un monitor del computer con pixel quadrati.

Quando l'applicazione Reader genera un video che verrà riprodotto in una televisione NTSC, ad esempio tramite una connessione S-video out sulla scheda video, è necessario modificare il rettangolo video in modo che l'immagine venga visualizzata correttamente sui pixel non quadrati della televisione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Per leggere e scrivere flussi video con pixel non quadrati**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




