---
description: Uso dellHigh-Definition audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Uso High-Definition audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3eac918929b6495401a0eeaee31fe6d7a01d2df0eced9866da829381392edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737334"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Uso High-Definition audio (Microsoft Media Foundation)

L'audio ad alta definizione, nel contesto dei codec audio multimediali Windows, è qualsiasi tipo di audio con più di due canali o più di 16 bit per campione. L'audio ad alta definizione è supportato dalle categorie Professional e lossless di [Windows Media Audio Encoder.](windowsmediaaudioencoder.md)

I tipi audio ad alta definizione non compressi vengono definiti usando la [**struttura WAVEFORMATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) **WAVEFORMATEXTENSIBLE** è un'estensione strutturata della [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85)) Quando si usano DMO, il membro **formattype** della struttura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) che descrive un tipo audio ad alta definizione deve essere impostato su WMCFORMAT WaveFormatEx, proprio come per l'audio normale; non esiste un identificatore di formato speciale per \_ **WAVEFORMATEXTENSIBLE.** Se un formato **usa WAVEFORMATEXTENSIBLE,** è necessario impostare il membro **cbSize** della struttura **WAVEFORMATEX** su 22.

Quando si Media Foundation, è possibile costruire il tipo di supporto corretto da una [**struttura WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) usando la funzione [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

I tipi di output multicanale supportati dal codec Professional Windows Media Audio 10 non usano [**WAVEFORMATEXTENSIBLE,**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))ma segnalano il numero corretto di canali e bit per campione nella [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85)) Come per tutti i tipi di audio che descrivono il contenuto Windows Audio multimediale compresso, sono aggiunte informazioni aggiuntive alla struttura **WAVEFORMATEX** usata dal decodificatore per la decompressione.

## <a name="decoding-high-definition-audio"></a>Decodifica di High-Definition audio

Per decodificare l'audio ad alta definizione, è necessario impostare la [proprietà MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) su VARIANT \_ TRUE. Se questa proprietà non è impostata, il decodificatore consegnerà contenuto stereo con un massimo di 16 bit per campione, indipendentemente dal formato compresso.

> [!Note]  
> L'audio ad alta definizione è supportato solo Windows XP, Windows Vista e versioni successive. Nelle versioni precedenti di Windows, Windows contenuto audio multimediale codificato con alta definizione viene visualizzato come audio a due canali con un massimo di 16 bit per campione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'audio](workingwithaudio.md)
</dt> </dl>

 

 
