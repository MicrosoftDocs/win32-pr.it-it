---
title: Lettura dell'audio multicanale
description: Lettura dell'audio multicanale
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lettura di audio multicanale
- ASF (Advanced Systems Format), lettura di audio multicanale
- ASF (Advanced Systems Format), lettura di audio multicanale
- ASF (Advanced Systems Format), audio multicanale
- ASF (formato avanzato dei sistemi), audio multicanale
- codec, lettura di audio multicanale
- audio multicanale, lettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729455"
---
# <a name="reading-multichannel-audio"></a>Lettura dell'audio multicanale

Il codec Windows Media Audio 9 Professional può codificare l'audio multicanale (più di due canali). Quando si legge un file con audio multicanale, è necessario configurare correttamente l'output o l'audio verrà recapitato a una qualità inferiore e in stereo. Per impostare un output per il recapito audio multicanale, è necessario impostare due impostazioni di output: g \_ wszEnableDiscreteOutput e g \_ wszSpeakerConfig.

Impostando g \_ wszEnableDiscreteOutput su **true** , il codec viene impostato in modo da fornire un output audio ad alta definizione. L'audio ad alta definizione è codificato dal codec Windows Media Audio 9 con esempi a 24 bit in stereo o più canali. Se questa impostazione è **false**, verrà recapitato solo l'output stereo a 16 bit.

Il numero di altoparlanti nel computer di riproduzione è impostato con g \_ wszSpeakerConfig. Questa impostazione è un valore **DWORD** impostato su una delle costanti del relatore DirectSound elencate nella tabella seguente. Per risolvere questi nomi costanti per il compilatore, è necessario includere DSOUND. h.



| Costante             | Valore      | Descrizione                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ diretto | 0x00000000 | L'audio viene passato direttamente, senza essere configurato per gli speaker. |
| \_cuffia DSSPEAKER | 0x00000001 | Il computer client è dotato di cuffie.                             |
| \_mono DSSPEAKER      | 0x00000002 | Il computer client è dotato di un altoparlante mono.                     |
| DSSPEAKER \_ quad      | 0x00000003 | Il computer client è dotato di altoparlanti quadrifonica.                  |
| DSSPEAKER \_ stereo    | 0x00000004 | Il computer client è dotato di altoparlanti stereo.                        |
| DSSPEAKER \_ surround  | 0x00000005 | Il computer client è dotato di altoparlanti con audio surround a quattro canali.   |
| \_5POINT1 DSSPEAKER   | 0x00000006 | Il computer client è dotato di cinque altoparlanti e un subwoofer.          |
| \_7POINT1 DSSPEAKER   | 0x00000007 | Il computer client è dotato di sette altoparlanti e un subwoofer.         |



 

Per impostare queste impostazioni, utilizzare [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Infine, affinché i canali vengano restituiti in modo discreto, senza riduzioni fino a stereo, è necessario impostare il tipo di supporto corretto nell'output attenendosi alla procedura seguente:

1.  Chiamare [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) per ottenere il numero di formati supportati per l'output audio pertinente. Gli indici del formato di output sono in base zero.
2.  Per ogni formato supportato, chiamare [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) per recuperare l'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) nell'oggetto proprietà del supporto di output.
3.  Chiamare [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) per recuperare il tipo di supporto.
4.  Se il tipo di supporto recuperato è il tipo multicanale desiderato, impostarlo chiamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Dopo aver impostato l'output discreto e la configurazione dell'altoparlante, i formati di output enumerati dal lettore devono includere formati multicanale che usano la struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) . Se si enumerano i formati di output prima di impostare le proprietà, verranno inclusi solo i formati con 1 o 2 canali e un massimo di 16 bit per canale. Come per gli altri formati audio, è consigliabile usare solo i formati enumerati dal lettore; non configurare il proprio.

> [!Note]  
> È possibile generare l'audio multicanale solo se l'applicazione è in esecuzione in Microsoft Windows XP o in una versione successiva di Microsoft Windows.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Impostazioni di output**](output-settings.md)
</dt> <dt>

[**Uso di High-Resolution audio PCM**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 