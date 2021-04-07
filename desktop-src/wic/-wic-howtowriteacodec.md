---
description: Questa sezione degli argomenti fornisce agli sviluppatori informazioni aggiuntive su come implementare i codec del formato di file di immagine che funzioneranno all'interno del Framework di Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Come scrivere un codec WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882194"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Come scrivere un codec WIC-Enabled

Questa sezione degli argomenti fornisce agli sviluppatori informazioni aggiuntive su come implementare i codec del formato di file di immagine che funzioneranno all'interno del Framework di Windows Imaging Component (WIC).

<dl>

[Introduzione](-wic-howtowriteacodec-intro.md)  
[Funzionamento di Windows Imaging Component (WIC)](-wic-howwicworks.md)  
<dl>

[Individuazione e arbitraggio](-wic-howwicworks.md)  
[Decodifica](-wic-howwicworks.md)  
[Encoding](-wic-howwicworks.md)  
[Durata di un codec](-wic-howwicworks.md)  
[Come abilitare WIC per un codec](-wic-howwicworks.md)  
[Supporto di Apartment multithread in WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementazione di un decodificatore WIC-Enabled</a><dl>

[Interfacce del decodificatore](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementazione di un codificatore di WIC-Enabled</a>  
<dl>

[Interfacce del codificatore](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Installazione e registrazione di codec</a>  
<dl>

[Registrazione di un codec](-wic-codecinstallandreg.md)  
<dl>

[Voci di registro generali](-wic-generalregentries.md)  
[Voci del registro di sistema specifiche del codificatore](-wic-encoderregentries.md)  
<dl>

[Registrazione di un formato contenitore con writer di metadati](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Voci del registro di sistema specifiche del codificatore</a>  
<dl>

[Registrazione di un nuovo formato del contenitore con i lettori di metadati](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Integrazione con la PhotoGallery di Windows Vista ed Esplora risorse</a>  
<dl>

[Archivio delle proprietà di Windows](-wic-integrationregentries.md)  
[Raccolta foto di Windows Vista](-wic-integrationregentries.md)  
[Cache anteprime di Windows Vista](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Aggiornamento della cache delle anteprime durante l'installazione di un codec</a> [rendere disponibile il codec WIC-Enabled per gli utenti](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Introduzione (come scrivere un CODEC WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



