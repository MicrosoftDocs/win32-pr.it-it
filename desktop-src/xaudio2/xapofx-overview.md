---
description: XAPOFX è una raccolta di effetti audio che implementa le interfacce XAPO da usare in XAudio2. XAPOFX contiene diversi effetti e un meccanismo comune per la creazione di istanze di effetto.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Panoramica di XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8979b5de50406d46bc472e18ca4a6479679e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526874"
---
# <a name="xapofx-overview"></a>Panoramica di XAPOFX

XAPOFX è una raccolta di effetti audio che implementa le interfacce [XAPO](xapo-overview.md) da usare in XAudio2. XAPOFX contiene diversi effetti e un meccanismo comune per la creazione di istanze di effetto.

## <a name="included-effects"></a>Effetti inclusi

Nella tabella seguente vengono descritti gli effetti inclusi in XAPOFX. 

| Effetto             | Descrizione                                                                                                                                                                                           | Struttura di parametri                                                     | Costanti parametro                                              | Requisiti                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Effetto Echo.                                                                                                                                                                                       | [**\_parametri FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Costanti FXECHO**](fxecho-constants.md)                     | Supporta solo formati audio FLOAT32.                                                                                      |
| FXEQ               | Equalizzatore A quattro bande.                                                                                                                                                                                | [**\_parametri FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Costanti FXEQ**](fxeq-constants.md)                         | Supporta solo formati audio FLOAT32. La frequenza di campionamento deve essere compresa tra 22.000 Hz e 48.000 Hz.                             |
| FXMasteringLimiter | Limite del volume.                                                                                                                                                                                     | [**\_parametri FXMASTERINGLIMITER**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Costanti FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Supporta solo formati audio FLOAT32.                                                                                      |
| FXReverb           | Un effetto di riverbero semplice.<br/> XAudio2 fornisce anche un effetto che implementa il Riverb digitale di Princeton di cui è possibile creare un'istanza con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**\_parametri FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Costanti FXREVERB**](fxreverb-constants.md)                 | Supporta solo formati audio FLOAT32. Supporta inoltre solo l'input mono per l'output mono e l'input stereo nell'output stereo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Creazione di un'istanza di un effetto incluso in XAPOFX

XAPOFX fornisce la funzione [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) come meccanismo comune per la creazione di istanze di effetto. **CreateFX** accetta il CLSID di un effetto e restituisce un puntatore a un'interfaccia IUnknown a un'istanza dell'effetto.

## <a name="using-xapofx-in-xaudio2"></a>Uso di XAPOFX in XAudio2

Gli effetti di cui è stata creata un'istanza con [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) vengono usati in XAudio2 mediante la connessione a voci. Ogni voce di XAudio2 ha una catena di effetti che contiene zero o più effetti audio. I dati audio inviati a una voce vengono passati attraverso ogni effetto della catena prima che vengano inviati alle destinazioni di output della voce. La voce prende l'output di ogni effetto e la inserisce nell'effetto successivo della catena fino a quando non vengono lasciati effetti nella catena. Per associare un effetto XAPOFX a una voce XAudio2, compilare una struttura [**a \_ \_ catena di effetti XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) con le informazioni sull'effetto e passarla a [**IXAudio2Voice:: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Per altre informazioni sulle catene di effetti XAudio2, vedere [effetti audio XAudio2](xaudio2-audio-effects.md).

Per un esempio dell'uso di XAPOFX in XAudio2, vedere [procedura: Usare XAPOFX in XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="xaudio2-implicit-effects"></a>Effetti impliciti XAudio2

Oltre alla libreria di XAPOs fornita da XAPOFX, XAudio2 include effetti audio del contatore e del contatore del volume predefiniti. È possibile creare questi effetti predefiniti con [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) e [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter). Vedere [procedura: creare una catena di effetti](how-to--create-an-effect-chain.md) per un esempio di utilizzo di uno di questi effetti predefiniti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> </dl>

 

 
