---
description: Windows Imaging Component (WIC) fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Panoramica del componente imaging Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231900"
---
# <a name="windows-imaging-component-overview"></a>Panoramica del componente imaging Windows

Windows Imaging Component (WIC) fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini. WIC rende possibile i fornitori di software indipendenti (ISV) e i fornitori di hardware indipendenti (IHV) per sviluppare i propri codec di immagine e ottenere lo stesso supporto della piattaforma dei formati di immagine standard (ad esempio, TIFF, JPEG, PNG, GIF, BMP e HDPhoto). Un unico set coerente di interfacce viene usato per tutte le operazioni di elaborazione delle immagini, indipendentemente dal formato di immagine, quindi qualsiasi applicazione che usa WIC ottiene il supporto automatico per i nuovi formati di immagine non appena viene installato il codec. Extensible Metadata Framework consente alle applicazioni di leggere e scrivere i propri metadati proprietari direttamente nei file di immagine, in modo che i metadati non vengano mai persi o separati dall'immagine.

In questo argomento sono incluse le sezioni seguenti.

-   [Funzionalità del componente Windows Imaging](#windows-imaging-component-features)
-   [Codec nativi](#native-codecs)
-   [Argomenti correlati](#related-topics)

## <a name="windows-imaging-component-features"></a>Funzionalità del componente Windows Imaging

Le funzionalità principali di WIC sono:

-   Consente agli sviluppatori di applicazioni di eseguire operazioni di elaborazione di immagini in qualsiasi formato di immagine tramite un unico set coerente di interfacce comuni, senza richiedere la conoscenza precedente di formati di immagine specifici.
-   Fornisce un'architettura "plug and Play" estendibile per codec di immagini, formati pixel e metadati, con l'individuazione automatica dei nuovi formati in fase di esecuzione.
-   Supporta la lettura e la scrittura di metadati arbitrari nei file di immagine, con la possibilità di mantenere i metadati non riconosciuti durante la modifica.
-   Conserva i dati di immagini con profondità elevata, fino a 32 bit per canale, in tutta la pipeline di elaborazione delle immagini.
-   Fornisce supporto incorporato per i formati di immagine più diffusi, i formati pixel e gli schemi di metadati.

## <a name="native-codecs"></a>Codec nativi

WIC include diversi codec predefiniti. Con la piattaforma vengono forniti i codec standard seguenti. 

| Codec                                                                                             | Tipi MIME                       | Decodificatori | Codificatori |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (formato bitmap Windows), specifica BMP V5.                                                | image/bmp                        | Sì      | Sì      |
| GIF (Graphics Interchange Format 89a), specifica GIF 89a/89m                                  | image/gif                        | Sì      | Sì      |
| ICO (formato icona)                                                                                 | immagine/ICO                        | Sì      | No       |
| JPEG (Joint Photographic Experts Group), specifica JFIF 1,02                                  | image/jpeg, image/JPE, image/jpg | Sì      | Sì      |
| PNG (Portable Network Graphics), specifica PNG 1,2                                            | image/png                        | Sì      | Sì      |
| TIFF (Tagged Image File Format), specifica TIFF 6,0                                           | image/TIFF, image/TIF            | Sì      | Sì      |
| Windows Media Photo, [specifiche foto HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | image/vnd. ms-phot                | Sì      | Sì      |
| DDS (superficie DirectDraw)                                                                          | image/vnd. ms-DDS                 | Sì      | Sì      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui metadati WIC](-wic-about-metadata.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[CODEC di esempio AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
