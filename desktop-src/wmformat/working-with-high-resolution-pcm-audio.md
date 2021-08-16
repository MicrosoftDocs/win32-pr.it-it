---
title: Uso di High-Resolution PCM Audio
description: Uso di High-Resolution PCM Audio
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF), audio PCM ad alta risoluzione
- ASF (Advanced Systems Format), audio PCM ad alta risoluzione
- profili, audio PCM ad alta risoluzione
- codec, audio PCM ad alta risoluzione
- Advanced Systems Format (ASF), audio PCM
- ASF (Advanced Systems Format), audio PCM
- profili,audio PCM
- codec, audio PCM
- audio PCM ad alta risoluzione
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a76cfb8397cacd6d39f62ea3594c8be655f4543e0b48b60cafbf15b9783c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194856"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Uso di High-Resolution PCM Audio

Alcuni dei formati di input per il codec Windows Media Audio 9 Professional e il codec Windows Media Audio 9 Lossless sono formati PCM ad alta risoluzione. Si tratta di formati PCM con più di due canali o più di 16 bit per campione (l'audio con più di due canali è detto anche audio multicanale).

Questi formati vengono configurati usando un'estensione strutturata della [**struttura WAVEFORMATEX,**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) denominata [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)). La **struttura WAVEFORMATEXTENSIBLE** include informazioni sui canali inclusi nell'audio. Questa struttura è necessaria quando si usa audio PCM ad alta risoluzione, perché alcune API Windows non accetteranno strutture **WAVEFORMATEX** che contengono valori ad alta risoluzione.

I formati PCM ad alta risoluzione hanno 22 byte di dati estesi, specificati nel membro **cbSize** della **struttura WAVEFORMATEX.** I formati audio Windows media ad alta risoluzione non usano la struttura **WAVEFORMATEXTENSIBLE,** ma hanno dati estesi aggiunti alla **struttura WAVEFORMATEX.**

I Windows audio multimediali supportano la decodifica in formati PCM ad alta risoluzione solo quando l'applicazione è in esecuzione Windows XP o versioni successive. Nelle versioni precedenti di Microsoft Windows, i codec decodificano in un formato con un massimo di 16 bit per campione e 2 canali. È inoltre necessario specificare che il codec deve decodificare in PCM ad alta definizione impostando l'impostazione di output g \_ wszEnableDiscreteOutput su **TRUE** usando il metodo [**IWMReaderAdvanced2::SetOutputSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) Dopo questa chiamata, gli output enumerati dal lettore includeranno formati ad alta definizione.

L'audio multicanale richiede una configurazione maggiore. Per altre informazioni, vedere [Lettura di audio multicanale.](reading-multichannel-audio.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso degli input**](working-with-inputs.md)
</dt> </dl>

 

 