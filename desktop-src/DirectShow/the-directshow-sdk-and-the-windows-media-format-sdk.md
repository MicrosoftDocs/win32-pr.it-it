---
description: DirectShow SDK e Windows Media Format SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: DirectShow SDK e Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351661"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>DirectShow SDK e Windows Media Format SDK

DirectShow e Windows Media Format SDK offrono soluzioni complementari per la scrittura di applicazioni per la creazione e la riproduzione di flussi di formato Windows Media. Per ulteriori informazioni, vedere la sezione "[audio e video](../audio-and-video.md)" di MSDN Library.

Il filtro del writer ASF accetta un numero qualsiasi di flussi di input e crea un file ASF. Il filtro usa Windows Media Format SDK per convertire i file audio o video non compressi in contenuto basato su Windows Media. Il contenuto compresso viene quindi archiviato nel formato del contenitore ASF. Se il contenuto è solo audio, al file viene assegnata un'estensione WMA e viene definito file di Windows Media Audio. Se il contenuto è solo video o video e audio, al file viene assegnata un'estensione. WMV e viene definito file di Windows Media Video. Entrambi i tipi di file possono includere anche i metadati.

È possibile usare il writer ASF WM in diversi scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di Audio-Video file multimediali con interfoliazione (AVI) o MPEG per lo streaming di rete. Questo filtro rappresenta l'unico modo per creare file di Microsoft® Windows Media™ Audio (WMA) e Windows Media Video (WMV) in DirectShow®. Il filtro può inoltre creare file protetti da Digital Rights Management (DRM) e può anche creare contenuti MPEG-4 usando il codificatore Microsoft MPEG-4. Questo contenuto è archiviato nel formato del contenitore ASF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
