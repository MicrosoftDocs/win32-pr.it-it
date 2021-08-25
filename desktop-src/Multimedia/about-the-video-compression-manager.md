---
title: Informazioni su Gestione compressione video
description: Informazioni su Gestione compressione video
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows multimediali, Gestione compressione video (VCM)
- multimediali, gestione compressione video (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122114666713b3bf5d1e706db2206a3d4894f8a40dea94d33d3b12829fb02bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808721"
---
# <a name="about-the-video-compression-manager"></a>Informazioni su Gestione compressione video

In genere, i programmi di compressione installabili funzionano con i dati delle immagini video archiviati in file AVI (Audio-Video Interleaved). In questa panoramica vengono illustrate le tecniche di programmazione usate per accedere ai compressi installabili tramite VCM e vengono trattati gli argomenti seguenti:

-   VCM e l'architettura video per Windows
-   Compressione e decompressione dei dati immagine dall'applicazione
-   Uso di renderer VCM per disegnare dati dall'applicazione
-   Funzioni e strutture di VCM

Prima di leggere questa panoramica, è necessario avere familiarità con i servizi grafici Microsoft Win32. In particolare, le bitmap e le strutture correlate alle bitmap, ad esempio [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) e [**BITMAPINFOHEADER,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)vengono usate ampiamente da VCM. Per altre informazioni sulle strutture **BITMAPINFO** e **BITMAPINFOHEADER,** vedere [Bitmap .](/previous-versions//ms532349(v=vs.85))

> [!Note]  
> Gestione compressione audio fornisce il supporto a livello di sistema per i driver di compressione e decompressione audio. Per una descrizione dei servizi di compressione audio, vedere [Gestione compressione audio](audio-compression-manager.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> </dl>

 

 