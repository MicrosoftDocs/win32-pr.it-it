---
description: Resampler audio esegue una o entrambe le azioni seguenti su un flusso audio. Modificare la frequenza di campionamento. Modificare il numero di canali.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: Audio Resampler DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf5e640ffd128a5b9249514284ecef16c5f57e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119415"
---
# <a name="audio-resampler-dsp"></a>Audio Resampler DSP

Resampler audio esegue una o entrambe le azioni seguenti su un flusso audio.

-   Modificare la frequenza di campionamento.
-   Modificare il numero di canali.

## <a name="clsid"></a>CLSID

CLSID \_ CResamplerMediaObject

## <a name="interfaces"></a>Interfacce

-   [**Oggetto IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formati

PCM o IEEE a virgola mobile

Il tipo di supporto deve specificare un formato audio PCM o a virgola mobile non compresso.

-   Per [**l'interfaccia IMFTransform,**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) inizializzare il tipo di supporto come descritto in [Tipi di supporti audio non compressi.](uncompressed-audio-media-types.md)
-   Per [**l'interfaccia IMediaObject,**](/previous-versions/ms785953%28v%3dvs.85%29) il tipo di supporto deve essere **un tipo FORMAT \_ WaveFormatEx.** Per altre informazioni, vedere [**DMO \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)

## <a name="properties"></a>Proprietà

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [MFPKEY \_ WMRESAMP \_ LOWPASS \_ BANDWIDTH](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Attributi obbligatori

Il resampler richiede che siano impostati gli attributi seguenti:

-   [MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK](mf-mt-audio-channel-mask-attribute.md)
-   [BYTE MEDIA AUDIO MF \_ MT \_ AL \_ \_ \_ \_ SECONDO](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [ALLINEAMENTO DEI \_ BLOCCHI AUDIO MF MT \_ \_ \_](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Mapping del canale personalizzato

Il resampler audio esegue il mapping dei canali audio di input ai canali audio di output, in base alle informazioni seguenti:

-   Il numero di canali. Questo valore è specificato [nell'attributo \_ MF MT \_ AUDIO NUM \_ \_ CHANNELS](mf-mt-audio-num-channels-attribute.md) del tipo di supporto o nel membro **nChannels** della [struttura WAVEFORMATEX.](mf-mt-audio-prefer-waveformatex-attribute.md)
-   Maschera del canale, che assegna i canali alla posizione del parlante. La channel mask viene specificata nell'attributo MF MT AUDIO CHANNEL MASK del tipo di supporto o nel membro \_ \_ \_ \_ **dwChannelMask** della [**struttura WAVEFORMATEXTENSIBLE.**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible)
-   Matrice di pesi di mapping.

La matrice contiene una serie di pesi, in modo che ogni canale di output sia una media ponderata dei canali di input.

È possibile specificare una matrice personalizzata per il mapping dei canali chiamando [**IWMResamplerProps::SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) o impostando la proprietà [**MFPKEY \_ WMRESAMP \_ CHANNELMTX.**](mfpkey-wmresamp-channelmtx.md) Se non viene specificata una matrice personalizzata, il resampler audio usa un set di matrici predefinite.

## <a name="default-channel-mapping"></a>Mapping dei canali predefinito

Se non si specifica una matrice personalizzata, il provider di servizi di configurazione Resampler audio usa i valori predefiniti per il mapping dei canali.

Nelle tabelle seguenti i canali sono abbreviati:

-   L: Left
-   R: A destra
-   C: Al centro
-   LFE: Effetti di frequenza bassa
-   BL: Back Left
-   BR: Indietro a destra
-   SL: Racchiudere a sinistra
-   SR: Racchiudere a destra

La tabella seguente illustra i coefficienti predefiniti per il mapping di 6 canali (maschera 0x3F) a 2 canali.



|     | L     | R     | C     | Lfe   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| **L**   | 0,314 | 0     | 0,222 | 0.031 | 0,268 | 0.164 |
| **R**   | 0     | 0,314 | 0,222 | 0.031 | 0.164 | 0,268 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 6 canali (maschera 0x60F) a 2 canali.



|     | L     | R     | C     | Lfe   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| **L**   | 0.320 | 0     | 0.226 | 0.032 | 0.292 | 0.130 |
| **R**   | 0     | 0.320 | 0.226 | 0.032 | 0.130 | 0.292 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 6 canali (maschera 0x3F o 0x60F) a 1 canale.



|     | L     | R     | C     | Lfe   | BL (SL) | BR (SR) |
|-----|-------|-------|-------|-------|--------|--------|
| **C**   | 0.192 | 0.192 | 0.192 | 0.038 | 0.192  | 0.192  |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (maschera 0x63F) a 2 canali.



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0,222 | 0     | 0.157 | 0.022 | 0,189 | 0.116 | 0.203 | 0.090 |
| **R**   | 0     | 0,222 | 0.157 | 0.022 | 0.116 | 0,189 | 0.090 | 0.203 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (maschera 0x63F) a 1 canale.



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **C**   | 0.139 | 0.139 | 0.139 | 0.028 | 0.139 | 0.139 | 0.139 | 0.139 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (maschera 0x63F) a 6 canali (maschera 0x3F).



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| **R**   | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| **C**   | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     | 0     |
| **Lfe** | 0     | 0     | 0     | 0.518 | 0     | 0     | 0     | 0     |
| **BL**  | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 | 0     |
| **Br**  | 0     | 0     | 0     | 0     | 0     | 0.518 | 0     | 0.482 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (maschera 0x63F) a 6 canali (maschera 0x60F).



|     | L     | R     | C     | Lfe   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| **L**   | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| **R**   | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     | 0     |
| **C**   | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     | 0     |
| **Lfe** | 0     | 0     | 0     | 0.447 | 0     | 0     | 0     | 0     |
| **SL**  | 0     | 0     | 0     | 0     | 0.429 | 0.124 | 0.447 | 0     |
| **SR**  | 0     | 0     | 0     | 0     | 0.124 | 0.429 | 0     | 0.447 |



 

Per comprendere come interpretare le tabelle dei coefficienti, prendere in considerazione la prima tabella, che esegue il mapping di 6 canali a 2. La prima riga della tabella (0,314, 0, 0,222, 0,031, 0,268, 0,164) è un vettore di pesi che specifica il peso di ogni canale di input che contribuisce al canale sinistro dell'output. La seconda riga della tabella (0, 0,314, 0,222, 0,031, 0,164, 0,268) è un vettore di pesi che specifica il livello di contributo di ogni canale di input al canale destro dell'output.

Le formule seguenti mostrano come vengono calcolati i canali di output.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Se si usa il provider di servizi di campionamento audio per aumentare il numero di canali, ai canali aggiunti verranno assegnati valori 0.

 

## <a name="output-quality"></a>Qualità dell'output

È possibile specificare la qualità di output del provider di servizi di campionamento audio chiamando [**IWMResamplerProps::SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) o impostando la proprietà [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY.**](mfpkey-wmresamp-filterquality.md) Se non si specifica la qualità di output, il provider di servizi di campionamento audio usa un valore di qualità predefinito pari a 30.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Vedere anche

[Processori di segnali digitali](windowsmediadigitalsignalprocessors.md)
