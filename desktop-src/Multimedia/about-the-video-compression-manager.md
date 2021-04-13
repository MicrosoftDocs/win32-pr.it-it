---
title: Informazioni su Gestione compressione video
description: Informazioni su Gestione compressione video
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows Multimedia, Gestione compressione video (VCM)
- Multimedia, Gestione compressione video (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472947"
---
# <a name="about-the-video-compression-manager"></a>Informazioni su Gestione compressione video

In genere, i compressori installabili operano con dati di immagini video archiviati in file audio-video con interfoliazione (AVI). In questa panoramica vengono illustrate le tecniche di programmazione utilizzate per accedere ai compressori installabili tramite VCM e vengono trattati gli argomenti seguenti:

-   VCM e il video per l'architettura di Windows
-   Compressione e decompressione dei dati dell'immagine dall'applicazione
-   Uso dei renderer di VCM per disegnare i dati dall'applicazione
-   Funzioni e strutture di VCM

Prima di leggere questa panoramica, è necessario avere familiarità con i servizi grafici di Microsoft Win32. In particolare, le bitmap e le strutture correlate a bitmap, ad esempio [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) e [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), vengono usate estensivamente da VCM. Per ulteriori informazioni sulle strutture **BITMAPINFO** e **BITMAPINFOHEADER** , vedere [bitmap](/previous-versions//ms532349(v=vs.85)).

> [!Note]  
> Audio Compression Manager (ACM) fornisce il supporto a livello di sistema per la compressione audio e i driver di decompressione. Per una descrizione dei servizi di compressione audio, vedere [Gestione compressione audio](audio-compression-manager.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> </dl>

 

 