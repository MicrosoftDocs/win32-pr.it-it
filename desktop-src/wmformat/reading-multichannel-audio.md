---
title: Lettura dell'audio multicanale
description: Lettura dell'audio multicanale
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lettura di audio multicanale
- Advanced Systems Format (ASF), lettura di audio multicanale
- ASF (Advanced Systems Format), lettura di audio multicanale
- Advanced Systems Format (ASF), audio multicanale
- ASF (Advanced Systems Format), audio multicanale
- codec, lettura di audio multicanale
- audio multicanale, lettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ba314c6f2579bb18cd73593a775089c4b04b1c4a8ecd34868af911da29a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658531"
---
# <a name="reading-multichannel-audio"></a>Lettura dell'audio multicanale

Il Windows Media Audio 9 Professional codifica audio multicanale (più di due canali). Quando si legge un file con audio multicanale, è necessario configurare correttamente l'output o l'audio verrà recapitato a una qualità inferiore e in stereo. Per impostare un output per il recapito audio multicanale, è necessario impostare due impostazioni di output: g \_ wszEnableDiscreteOutput e g \_ wszSpeakerConfig.

L'impostazione \_ di g wszEnableDiscreteOutput su **TRUE** imposta il codec per fornire output audio ad alta definizione. L'audio ad alta definizione viene codificato dal codec Windows Media Audio 9 con esempi a 24 bit in canali stereo o multipli. Se questa impostazione è **FALSE,** verrà recapitato solo l'output stereo a 16 bit.

Il numero di altoparlanti nel computer in riproduzione è impostato con g \_ wszSpeakerConfig. Questa impostazione è un **valore DWORD** impostato su una delle costanti voce DirectSound elencate nella tabella seguente. Per risolvere questi nomi di costanti per il compilatore, è necessario includere dsound.h.



| Costante             | Valore      | Descrizione                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | L'audio viene passato direttamente, senza essere configurato per gli altoparlanti. |
| CUFFIA DSSPEAKER \_ | 0x00000001 | Il computer client è dotato di cuffia.                             |
| DSSPEAKER \_ MONO      | 0x00000002 | Il computer client è dotato di un altoparlante monaural.                     |
| DSSPEAKER \_ QUAD      | 0x00000003 | Il computer client è dotato di altoparlanti quadrafone.                  |
| DSSPEAKER \_ STEREO    | 0x00000004 | Il computer client è dotato di altoparlanti stereo.                        |
| DSSPEAKER \_ SURROUND  | 0x00000005 | Il computer client è dotato di altoparlanti surround a quattro canali.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | Il computer client è dotato di cinque altoparlanti e di un subwoofer.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | Il computer client è dotato di sette altoparlanti e di un subwoofer.         |



 

Per impostare queste impostazioni, usare [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Infine, per l'output discreto dei canali, senza ripiegare su stereo, è necessario impostare il tipo di supporto corretto nell'output seguendo questa procedura:

1.  Chiamare [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) per ottenere il numero di formati supportati per l'output audio pertinente. Gli indici del formato di output sono in base zero.
2.  Per ogni formato supportato, chiamare [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) per recuperare [**l'interfaccia IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) nell'oggetto proprietà del supporto di output.
3.  Chiamare [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) per recuperare il tipo di supporto.
4.  Se il tipo di supporto recuperato è il tipo multicanale desiderato, impostarlo chiamando [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Dopo aver impostato l'output discreto e la configurazione del parlante, i formati di output enumerati dal lettore devono includere formati multicanale che usano la [**struttura WAVEFORMATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) Se si enumerano i formati di output prima di impostare le proprietà , verranno inclusi solo i formati con 1 o 2 canali e un massimo di 16 bit per canale. Come per altri formati audio, è consigliabile usare solo i formati enumerati dal lettore. non configurare il proprio.

> [!Note]  
> È possibile eseguire l'output audio multicanale solo se l'applicazione è in esecuzione in Microsoft Windows XP o una versione successiva di Microsoft Windows.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Input, Flussi e output**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Output Impostazioni**](output-settings.md)
</dt> <dt>

[**Uso di High-Resolution PCM Audio**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 