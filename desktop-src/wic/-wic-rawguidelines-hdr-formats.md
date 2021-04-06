---
description: Formati pixel con intervallo dinamico elevato
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formati pixel con intervallo dinamico elevato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883966"
---
# <a name="high-dynamic-range-pixel-formats"></a>Formati pixel con intervallo dinamico elevato

I codec devono usare formati pixel di Windows Imaging Component (WIC) che conservano tutti gli intervalli dinamici dei dati dei sensori sottostanti. GUID \_ WICPixelFormat48bppRGB è un tipico formato a virgola fissa a 16 bit per canale che può essere utilizzato. È anche possibile usare altri formati con precisione più elevata. Per abilitare il supporto completo per la pipeline di rendering con accelerazione della Windows Presentation Foundation GPU (Graphics Processing Unit), Microsoft consiglia vivamente di supportare un formato pixel a virgola mobile a 32 bit.

Formati pixel di colore elevato: con Windows 7 sono stati aggiunti due nuovi formati pixel WIC per supportare i nuovi formati di visualizzazione a colori elevati. Ovvero GUID \_ WICPixelFormat32bppRGBA1010102 e GUID \_ WICPixelFormat32bppRGBA1010102XR.

Il formato a colori elevato float a 16 bit per canale (bpc) è supportato dal \_ formato pixel WICPIXELFORMAT64BPPRGBAHALF GUID esistente.

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

 

 



