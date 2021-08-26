---
description: XAPOFX è una raccolta di effetti audio che implementano le interfacce XAPO da usare in XAudio2. XAPOFX contiene diversi effetti e un meccanismo comune per la creazione di istanze degli effetti.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Panoramica di XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae339a022ae5e2e880dcd130dbe055d0fde9cd28a95ea52c1238e2ade080ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005721"
---
# <a name="xapofx-overview"></a>Panoramica di XAPOFX

XAPOFX è una raccolta di effetti audio che implementano le [interfacce XAPO](xapo-overview.md) da usare in XAudio2. XAPOFX contiene diversi effetti e un meccanismo comune per la creazione di istanze degli effetti.

## <a name="included-effects"></a>Effetti inclusi

La tabella seguente descrive gli effetti inclusi in XAPOFX. 

| Effetto             | Descrizione                                                                                                                                                                                           | Struttura dei parametri                                                     | Costanti dei parametri                                              | Requisiti                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Effetto echo.                                                                                                                                                                                       | [**PARAMETRI \_ FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Costanti FXECHO**](fxecho-constants.md)                     | Supporta solo i formati audio FLOAT32.                                                                                      |
| FXEQ               | Equalizzatore a quattro bande.                                                                                                                                                                                | [**PARAMETRI \_ FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Costanti FXEQ**](fxeq-constants.md)                         | Supporta solo i formati audio FLOAT32. La frequenza di campionamento deve essere compresa tra 22.000 Hz e 48.000 Hz.                             |
| FXMasteringLimiter | Limitatore di volume.                                                                                                                                                                                     | [**PARAMETRI FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Costanti FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Supporta solo i formati audio FLOAT32.                                                                                      |
| FXReverb           | Un semplice effetto di riverbero.<br/> XAudio2 fornisce anche un effetto che implementa Il riverbero digitale di Princeton di cui è possibile creare un'istanza [**con XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**PARAMETRI \_ FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Costanti FXREVERB**](fxreverb-constants.md)                 | Supporta solo i formati audio FLOAT32. Supporta anche solo l'input mono per l'output mono e l'input stereo per l'output stereo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Creazione di un'istanza di un effetto incluso in XAPOFX

XAPOFX fornisce la [**funzione CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) come meccanismo comune per la creazione di istanze dell'effetto. **CreateFX** accetta il CLSID di un effetto e restituisce un puntatore a interfaccia IUnknown a un'istanza dell'effetto.

## <a name="using-xapofx-in-xaudio2"></a>Uso di XAPOFX in XAudio2

Gli effetti di cui [**viene creata un'istanza**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) con CreateFX vengono usati in XAudio2 collegandoli alle voci. Ogni voce XAudio2 ha una catena di effetti contenente zero o più effetti audio. I dati audio inviati a una voce vengono passati attraverso ogni effetto nella catena prima di essere inviati alle destinazioni di output della voce. La voce accetta l'output di ogni effetto e lo alimenta nell'effetto successivo nella catena fino a quando non viene lasciato alcun effetto nella catena. Per associare un effetto XAPOFX a una voce XAudio2, compilare una struttura [**XAUDIO2 \_ EFFECT \_ CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con le informazioni dell'effetto e passarlo a [**IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Per altre informazioni sulle catene di effetti XAudio2, vedere [Effetti audio XAudio2](xaudio2-audio-effects.md).

Per un esempio di uso di XAPOFX in XAudio2, vedere [Procedura: Usare XAPOFX in XAudio2.](how-to--use-xapofx-in-xaudio2.md)

## <a name="xaudio2-implicit-effects"></a>Effetti impliciti XAudio2

Oltre alla libreria di XAPO fornita da XAPOFX, XAudio2 ha effetti audio di riverbero e contatore del volume predefiniti. È possibile creare questi effetti predefiniti con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) e [**XAudio2CreateVolumeMeter.**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) Vedere [Procedura: Creare una catena di](how-to--create-an-effect-chain.md) effetti per un esempio di uso di uno di questi effetti predefiniti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> </dl>

 

 
