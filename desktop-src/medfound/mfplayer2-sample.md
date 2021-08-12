---
description: Importante Deprecato.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Esempio di MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ead2df415af1584f34661a0c1d18751350d59bd1a94ac48f41d3bf9dca2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241733"
---
# <a name="mfplayer2-sample"></a>Esempio di MFPlayer2

> [!IMPORTANT]
> Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows. Le applicazioni devono usare la [sessione multimediale per](media-session.md) la riproduzione.

 

Illustra alcune delle funzionalità di riproduzione omesse [dall'esempio SimplePlay,](simpleplay-sample.md) ad esempio:

-   riercare
-   Controllo della frequenza (avanzamento rapido e riavvolgimento)
-   Controlli volume audio e disattivazione audio
-   Zoom video

L'immagine seguente mostra i controlli usati per queste funzionalità.

![Screenshot dell'esempio mfplayer ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

Questo esempio illustra le API seguenti.

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**IAudioSessionManager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
