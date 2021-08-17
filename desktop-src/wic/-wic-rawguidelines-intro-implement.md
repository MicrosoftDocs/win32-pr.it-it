---
description: Linee guida generali per l'implementazione di codec RAW
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Linee guida generali per l'implementazione di codec RAW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5081edfc6f49dc1d145fc3e2ce7e5f993fb2e7e250aeb0f1091579dd3f45461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204629"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Linee guida generali per l'implementazione di codec RAW

Rispetto ai tipi di immagine non RAW, ad esempio JPEG o TIFF, esistono due differenze significative nel comportamento previsto dei formati di immagine RAW Windows:

-   Si presuppone che la maggior parte dei formati di immagine RAW sia di "sola lettura" e probabilmente non supporterà la codifica dei pixel in formato RAW. Tuttavia, poiché Windows Imaging Component (WIC) richiede un codificatore per supportare il write-back dei metadati, gli autori di codec RAW devono pianificare l'implementazione di almeno una classe di codificatore scheletro.
-   La decodifica di un'immagine RAW di dimensioni complete può richiedere molto tempo rispetto ad altri formati. Per questo motivo, Microsoft consiglia di usare alcuni approcci per ridurre al minimo la latenza di decodifica e per garantire il supporto per scenari come il rendering rapido di anteprime e anteprime.

    Ad esempio, tutti gli autori di codec RAW devono implementare [**l'interfaccia IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) che fornisce un meccanismo per notificare al decodificatore prima delle dimensioni della bitmap di destinazione, consentendo la decodifica ottimizzata a dimensioni dell'immagine di output inferiori.

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

 

 



