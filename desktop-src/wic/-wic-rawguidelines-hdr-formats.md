---
description: High Dynamic Range formati pixel
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: High Dynamic Range formati pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086914"
---
# <a name="high-dynamic-range-pixel-formats"></a>High Dynamic Range formati pixel

I codec devono usare Windows di pixel WIC (Imaging Component) che mantengono tutto l'intervallo dinamico dei dati del sensore sottostante. GUID \_ WICPixelFormat48bppRGB è un tipico formato a 16 bit per canale a 16 bit che può essere usato. È possibile usare anche altri formati di precisione superiore. Per abilitare il supporto completo per la pipeline di rendering con accelerazione GPU (Graphics Processing Unit) di Windows Presentation Foundation, Microsoft consiglia vivamente il supporto per un formato pixel a virgola mobile a 32 bit.

Formati pixel a colori elevati: con Windows 7, sono stati aggiunti due nuovi formati di pixel WIC per supportare i nuovi formati di visualizzazione a colori elevati. Questi sono: GUID \_ WICPixelFormat32bppRGBA1010102 e GUID \_ WICPixelFormat32bppRGBA1010102XR.

Il formato a 16 bit per canale (bpc) float High Color è supportato dal formato \_ pixel WICPixelFormat64bppRGBAHalf GUID esistente.

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

 

 



