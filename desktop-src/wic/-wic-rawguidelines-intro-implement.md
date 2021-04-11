---
description: Linee guida generali per l'implementazione di codec non ELABORAti
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Linee guida generali per l'implementazione di codec non ELABORAti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232878"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Linee guida generali per l'implementazione di codec non ELABORAti

Rispetto ai tipi di immagine non ELABORAti, ad esempio JPEG o TIFF, esistono due differenze significative nel modo in cui si prevede che i formati di immagine RAW si comportino in Windows:

-   La maggior parte dei formati di immagine non ELABORAta si presume essere di sola lettura e probabilmente non supporterà la codifica pixel in formato non elaborato. Tuttavia, poiché Windows Imaging Component (WIC) richiede che un codificatore supporti il writeback dei metadati, gli autori di codec non ELABORAti devono pianificare l'implementazione di almeno una classe Skeleton Encoder.
-   La decodifica di un'immagine RAW a dimensione intera può richiedere molto tempo rispetto ad altri formati. Per questo motivo, Microsoft consiglia di adottare determinati approcci per ridurre al minimo la latenza di decodifica e per garantire il supporto per scenari come il rendering rapido di anteprime e anteprime.

    Tutti gli autori di codec RAW, ad esempio, devono implementare l'interfaccia [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , che fornisce un meccanismo per inviare una notifica al decodificatore in anticipo rispetto alla dimensione bitmap di destinazione, consentendo così la decodifica ottimizzata a una dimensione dell'immagine di output inferiore.

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

 

 



