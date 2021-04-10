---
title: Uso di High-Resolution audio PCM
description: Uso di High-Resolution audio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), audio PCM a risoluzione elevata
- ASF (Advanced Systems Format), audio PCM ad alta risoluzione
- profili, audio PCM ad alta risoluzione
- codec, audio PCM ad alta risoluzione
- ASF (Advanced Systems Format), audio PCM
- ASF (formato avanzato dei sistemi), audio PCM
- profili, audio PCM
- codec, audio PCM
- audio PCM ad alta risoluzione
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963198"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Uso di High-Resolution audio PCM

Alcuni formati di input per il codec Windows Media Audio 9 Professional e il codec Windows Media Audio 9 Lossless sono formati PCM ad alta risoluzione. Si tratta di formati PCM con più di due canali o più di 16 bit per campione (l'audio con più di due canali è denominato anche audio multicanale).

Questi formati sono configurati utilizzando un'estensione strutturata della struttura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , denominata [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)). La struttura **WAVEFORMATEXTENSIBLE** include informazioni sui canali inclusi nell'audio. Questa struttura è obbligatoria quando si usa audio PCM ad alta risoluzione, perché alcune API Windows non accettano strutture **WAVEFORMATEX** che contengono valori ad alta risoluzione.

I formati PCM ad alta risoluzione hanno 22 byte di dati estesi, specificati nel membro **cbSize** della struttura **WAVEFORMATEX** . I formati audio Windows Media ad alta risoluzione non usano la struttura **WAVEFORMATEXTENSIBLE** , ma hanno dati estesi aggiunti alla struttura **WAVEFORMATEX** .

I codec audio Windows Media supportano solo la decodifica in formati PCM ad alta risoluzione quando l'applicazione è in esecuzione in Windows XP o versione successiva. Nelle versioni precedenti di Microsoft Windows, i codec decodificano in un formato con un massimo di 16 bit per campione e 2 canali. Inoltre, è necessario specificare che si vuole che il codec decodifichi il PCM ad alta definizione impostando l' \_ impostazione di output g wszEnableDiscreteOutput su **true** usando il metodo [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . Dopo aver effettuato questa chiamata, gli output enumerati dal reader includeranno formati ad alta definizione.

L'audio multicanale richiede una maggiore configurazione. Per ulteriori informazioni, vedere [lettura di audio multicanale](reading-multichannel-audio.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> </dl>

 

 