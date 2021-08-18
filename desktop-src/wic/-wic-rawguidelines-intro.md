---
description: Introduzione (linee guida WIC per i formati di immagine RAW della fotocamera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduzione (linee guida WIC per i formati di immagine RAW della fotocamera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96da37d36fed6af0aef271471eb2a0e5dae44bef71dfe14a4da37eba3f658c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086864"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introduzione (linee guida WIC per i formati di immagine RAW della fotocamera)

Il Windows Imaging Component (WIC) fornisce un framework estendibile per l'uso di immagini e metadati delle immagini. WiC consente ai fornitori di software e hardware di sviluppare codec in modo che i propri formati di immagine possano ottenere lo stesso supporto della piattaforma dei formati di immagine nativi, ad esempio TIFF (Tagged Image File Format), Joint Photographic Experts Group (JPEG) o HD Photo.

WIC fornisce un unico set coerente di interfacce per l'elaborazione di tutte le immagini, indipendentemente dal formato dell'immagine. Pertanto, qualsiasi applicazione che usa WIC riceve il supporto automatico per i nuovi formati di immagine non appena viene installato il codec. WIC offre anche un framework di metadati estendibile che consente alle applicazioni di leggere e scrivere i propri metadati proprietari direttamente nei file di immagine, in modo che i metadati non andranno mai persi o separati dall'immagine.

WIC è incluso in Windows Presentation Foundation (WPF) ed è integrato in Windows Vista e versioni Windows successive. È disponibile anche come componente ridistribuibile autonomo per Windows XP.

Queste linee guida sono progettate per aiutare i produttori di formati RAW nello sviluppo di codec WIC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



