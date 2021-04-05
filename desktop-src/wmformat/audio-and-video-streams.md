---
title: Flussi audio e video
description: Flussi audio e video
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK, flussi audio
- Formati di sistemi avanzati (ASF), flussi audio
- ASF (formato avanzato dei sistemi), flussi audio
- Windows Media Format SDK, flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- flussi audio, informazioni
- flussi video, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044645"
---
# <a name="audio-and-video-streams"></a>Flussi audio e video

I tipi più comuni di flussi usati nei file creati usando Windows Media Format SDK sono flussi audio e video. Le rappresentazioni digitali dei dati audio e video sono complesse e utilizzano grandi quantità di memoria. Nella maggior parte dei casi, audio e video vengono compressi prima di essere aggiunti a un file ASF. La compressione viene eseguita usando un compressore/decompressore (codec).

Con questo SDK sono inclusi diversi codec Windows Media e forniscono una compressione di qualità eccellente per i supporti digitali. Per ulteriori informazioni sui codec Windows Media, vedere funzionalità di [codec](codec-features.md). Molti altri codec sono disponibili da varie origini. È possibile usare qualsiasi codec, ad esempio, durante la creazione di file ASF, ma solo i codec Windows Media sono supportati direttamente dagli oggetti di questo SDK. Per usare altri codec, è necessario comprimere gli esempi e passarli all'oggetto writer come dati arbitrari.

La differenza più importante tra flussi audio o video e flussi arbitrari è che i flussi contenenti dati audio o video di Windows Media vengono convalidati dagli oggetti di Windows Media Format SDK. I flussi di dati arbitrari non vengono convalidati automaticamente e devono essere controllati per verificare l'integrità dell'applicazione.

Le proprietà di un flusso audio o video sono descritte nel profilo usato per creare il file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi arbitrari**](arbitrary-streams.md)
</dt> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




