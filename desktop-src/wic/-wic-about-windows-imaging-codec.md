---
description: Il Windows Imaging Component (WIC) fornisce un framework estendibile per l'uso di immagini e metadati delle immagini.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows Panoramica del componente di creazione dell'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f4276a70b94fd190b7254d8d3d2666581c0c9dbb991dee3ac6e0568b6ee649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772511"
---
# <a name="windows-imaging-component-overview"></a>Windows Panoramica del componente di creazione dell'immagine

Il Windows Imaging Component (WIC) fornisce un framework estendibile per l'uso di immagini e metadati delle immagini. WIC consente ai fornitori di software indipendenti (ISV) e ai fornitori di hardware indipendenti (IHV) di sviluppare codec di immagine personalizzati e ottenere lo stesso supporto della piattaforma dei formati di immagine standard (ad esempio, TIFF, JPEG, PNG, GIF, BMP e HDPhoto). Un singolo set coerente di interfacce viene usato per l'elaborazione di tutte le immagini, indipendentemente dal formato dell'immagine, quindi qualsiasi applicazione che usa il WIC ottiene il supporto automatico per i nuovi formati di immagine non appena viene installato il codec. Il framework di metadati estendibile consente alle applicazioni di leggere e scrivere i propri metadati proprietari direttamente nei file di immagine, in modo che i metadati non andranno mai persi o separati dall'immagine.

In questo argomento sono incluse le sezioni seguenti.

-   [Windows Funzionalità dei componenti di creazione dell'immagine](#windows-imaging-component-features)
-   [Codec nativi](#native-codecs)
-   [Argomenti correlati](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows Funzionalità dei componenti di creazione dell'immagine

Le funzionalità principali di WIC sono:

-   Consente agli sviluppatori di applicazioni di eseguire operazioni di elaborazione delle immagini in qualsiasi formato di immagine tramite un unico set coerente di interfacce comuni, senza che sia necessario conoscere in precedenza formati di immagine specifici.
-   Fornisce un'architettura "Plug and Play" estendibile per codec di immagini, formati pixel e metadati, con individuazione automatica dei nuovi formati in fase di esecuzione.
-   Supporta la lettura e la scrittura di metadati arbitrari nei file di immagine, con la possibilità di mantenere i metadati non riconosciuti durante la modifica.
-   Mantiene i dati di immagine ad alta profondità in bit, fino a 32 bit per canale, in tutta la pipeline di elaborazione delle immagini.
-   Fornisce supporto predefinito per i formati di immagine, i formati pixel e gli schemi di metadati più diffusi.

## <a name="native-codecs"></a>Codec nativi

WIC include diversi codec predefiniti. Con la piattaforma vengono forniti i codec standard seguenti. 

| Codec                                                                                             | Tipi Mime                       | Decoder | Codificatori |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (Windows Bitmap Format), BMP Specification v5.                                                | image/bmp                        | Sì      | Sì      |
| GIF (Graphics Interchange Format 89a), specifica GIF 89a/89m                                  | image/gif                        | Sì      | Sì      |
| ICO (formato icona)                                                                                 | image/ico                        | Sì      | No       |
| JPEG (Joint Photographic Experts Group), specifica JFIF 1.02                                  | image/jpeg, image/jpe, image/jpg | Sì      | Sì      |
| PNG (Portable Network Graphics), specifica PNG 1.2                                            | image/png                        | Sì      | Sì      |
| TIFF (Tagged Image File Format), specifica TIFF 6.0                                           | image/tiff, image/tif            | Sì      | Sì      |
| Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | image/vnd.ms-phot                | Sì      | Sì      |
| DDS (superficie DirectDraw)                                                                          | image/vnd.ms-dds                 | Sì      | Sì      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Codec di esempio AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
