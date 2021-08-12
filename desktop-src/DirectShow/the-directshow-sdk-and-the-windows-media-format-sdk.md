---
description: L DirectShow SDK e l'SDK Windows Media Format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: L DirectShow SDK e l'SDK Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651758"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>L DirectShow SDK e l'SDK Windows Media Format

DirectShow e l'SDK Windows Media Format offrono soluzioni complementari per la scrittura di applicazioni che creano e riproducino flussi Windows Media Format. Per altre informazioni, vedere la sezione "[Audio e video](../audio-and-video.md)" di MSDN Library.

Il filtro ASF Writer accetta un numero qualsiasi di flussi di input e crea un file ASF. Il filtro usa l'SDK Windows Media Format per convertire file audio o video non compressi Windows contenuto basato su media. Il contenuto compresso viene quindi archiviato nel formato del contenitore ASF. Se il contenuto è solo audio, al file viene data l'estensione wma e viene fatto riferimento come file audio Windows multimediale. Se il contenuto è solo video o video e audio, al file viene data l'estensione wmv e viene fatto riferimento come file video Windows multimediale. Entrambi i tipi di file possono includere anche metadati.

È possibile usare WM ASF Writer in diversi scenari, tra cui acquisizione di video digitali (DV), ricompressione audio e conversione di file multimediali Audio-Video Interleaved (AVI) o MPEG per lo streaming di rete. Questo filtro offre l'unico modo per creare file WMA (Microsoft® Windows Media™ Audio e Windows Media Video (WMV) in DirectShow®. Il filtro può anche creare file protetti da Digital Rights Management (DRM) e può anche creare contenuto MPEG-4 usando il codificatore Microsoft MPEG-4. Questo contenuto viene archiviato nel formato del contenitore ASF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
