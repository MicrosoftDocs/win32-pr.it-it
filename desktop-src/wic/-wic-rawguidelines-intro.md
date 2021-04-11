---
description: Introduzione (linee guida per WIC per i formati di immagini RAW della fotocamera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduzione (linee guida per WIC per i formati di immagini RAW della fotocamera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232876"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introduzione (linee guida per WIC per i formati di immagini RAW della fotocamera)

Windows Imaging Component (WIC) fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini. WIC consente ai fornitori di software e hardware di sviluppare codec in modo che i propri formati di immagine possano ottenere lo stesso supporto della piattaforma dei formati di immagine nativi, ad esempio il formato TIFF (Tagged Image File Format), il Joint Photographic Experts Group (JPEG) o la foto HD.

WIC fornisce un unico set coerente di interfacce per tutte le operazioni di elaborazione delle immagini, indipendentemente dal formato di immagine. Pertanto, qualsiasi applicazione che utilizza WIC riceve il supporto automatico per i nuovi formati di immagine non appena viene installato il codec. WIC fornisce anche un Framework di metadati estendibile che consente alle applicazioni di leggere e scrivere i propri metadati proprietari direttamente nei file di immagine, in modo che i metadati non vengano mai persi o separati dall'immagine.

WIC è incluso in Windows Presentation Foundation (WPF) ed è integrato in Windows Vista e versioni successive di Windows. È inoltre disponibile come componente ridistribuibile autonomo per Windows XP.

Queste linee guida sono progettate per aiutare i produttori di formati RAW a sviluppare codec WIC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



