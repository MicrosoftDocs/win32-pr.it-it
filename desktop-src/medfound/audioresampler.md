---
description: Il ricampionatore audio esegue una o entrambe le azioni seguenti in un flusso audio. Modificare la frequenza di campionamento. Modificare il numero di canali.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: Audio Resampler DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb173fa4f8d964bec1102c4cfeefa4bf83f1ffe
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321008"
---
# <a name="audio-resampler-dsp"></a>DSP ricampionatore audio

Il ricampionatore audio esegue una o entrambe le azioni seguenti in un flusso audio.

-   Modificare la frequenza di campionamento.
-   Modificare il numero di canali.

## <a name="clsid"></a>CLSID

\_CRESAMPLERMEDIAOBJECT CLSID

## <a name="interfaces"></a>Interfacce

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formati

PCM o IEEE a virgola mobile

Il tipo di supporto deve specificare un PCM non compresso o un formato audio a virgola mobile.

-   Per l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , inizializzare il tipo di supporto come descritto in [tipi di supporti audio non compressi](uncompressed-audio-media-types.md).
-   Per l'interfaccia [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) , il tipo di supporto deve essere un tipo **\_ WAVEFORMATEX di formato** . Per ulteriori informazioni, vedere [**DMO \_ media \_ Type**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Proprietà

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [\_larghezza di banda MFPKEY WMRESAMP- \_ basso \_](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Attributi obbligatori

Per il Resampler è necessario impostare i seguenti attributi:

-   [\_ \_ \_ maschera canale audio MF \_ mt](mf-mt-audio-channel-mask-attribute.md)
-   [\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [\_ \_ \_ allineamento blocchi audio MF \_ mt](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Mapping del canale personalizzato

Il Resampler audio esegue il mapping dei canali audio di input ai canali audio di output, in base alle informazioni seguenti:

-   Il numero di canali. Questa operazione viene fornita nell'attributo [MF \_ mt \_ audio \_ num \_ Channels](mf-mt-audio-num-channels-attribute.md) del tipo di supporto o del membro **nChannels** della struttura [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) .
-   La maschera del canale, che assegna i canali alla posizione dell'altoparlante. La maschera di canale viene specificata nell' \_ \_ \_ \_ attributo della maschera di canale audio MF mt del tipo di supporto o del membro **dwChannelMask** della struttura [**WAVEFORMATEXTENSIBLE**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) .
-   Matrice di pesi di mapping.

La matrice contiene una serie di pesi, in modo che ogni canale di output sia una media ponderata dei canali di input.

È possibile specificare una matrice personalizzata per il mapping del canale chiamando [**IWMResamplerProps:: SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) o impostando la proprietà [**MFPKEY \_ WMRESAMP \_ CHANNELMTX**](mfpkey-wmresamp-channelmtx.md) . Se non viene specificata una matrice personalizzata, il ricampionatore audio utilizza un set di matrici predefinite.

## <a name="default-channel-mapping"></a>Mapping del canale predefinito

Se non si specifica una matrice personalizzata, il DSP del Resampler audio utilizza i valori predefiniti per il mapping dei canali.

Nelle tabelle che seguono, i canali sono abbreviati:

-   L: sinistra
-   R: a destra
-   C: al centro
-   LFE: effetti a bassa frequenza
-   BL: indietro a sinistra
-   BR: indietro a destra
-   SL: surround a sinistra
-   SR: surround a destra

La tabella seguente illustra i coefficienti predefiniti per il mapping di 6 canali (mask 0x3F) a 2 canali.



|     | L     | R     | C     | LFE   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,314 | 0     | 0,222 | 0,031 | 0,268 | 0,164 |
| R   | 0     | 0,314 | 0,222 | 0,031 | 0,164 | 0,268 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 6 canali (mask 0x60F) a 2 canali.



|     | L     | R     | C     | LFE   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,320 | 0     | 0,226 | 0,032 | 0,292 | 0,130 |
| R   | 0     | 0,320 | 0,226 | 0,032 | 0,130 | 0,292 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di canali 6 (mask 0x3F o 0x60F) a 1 canale.



|     | L     | R     | C     | LFE   | BL (SL) | BR (SR) |
|-----|-------|-------|-------|-------|--------|--------|
| C   | 0,192 | 0,192 | 0,192 | 0,038 | 0,192  | 0,192  |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (mask 0x63F) a 2 canali.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,222 | 0     | 0,157 | 0,022 | 0,189 | 0,116 | 0,203 | 0,090 |
| R   | 0     | 0,222 | 0,157 | 0,022 | 0,116 | 0,189 | 0,090 | 0,203 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (mask 0x63F) a 1 Channel.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| C   | 0,139 | 0,139 | 0,139 | 0,028 | 0,139 | 0,139 | 0,139 | 0,139 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (mask 0x63F) a 6 canali (mask 0x3F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| R   | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| C   | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     |
| BL  | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 | 0     |
| BR  | 0     | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 |



 

La tabella seguente illustra i coefficienti predefiniti per il mapping di 8 canali (mask 0x63F) a 6 canali (mask 0x60F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| R   | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     |
| C   | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     |
| SL  | 0     | 0     | 0     | 0     | 0,429 | 0,124 | 0,447 | 0     |
| SR  | 0     | 0     | 0     | 0     | 0,124 | 0,429 | 0     | 0,447 |



 

Per comprendere come interpretare le tabelle dei coefficienti, si consideri la prima tabella che esegue il mapping di 6 canali a 2. La prima riga della tabella (0,314, 0, 0,222, 0,031, 0,268, 0,164) è un vettore di pesi che specifica il modo in cui ogni canale di input contribuisce al canale sinistro dell'output. La seconda riga della tabella (0, 0,314, 0,222, 0,031, 0,164, 0,268) è un vettore di pesi che specifica il modo in cui ogni canale di input contribuisce al canale corretto dell'output.

Nelle formule seguenti viene illustrato come vengono calcolati i canali di output.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Se si usa il DSP Audio Resampler per aumentare il numero di canali, ai canali aggiunti verranno assegnati valori pari a 0.

 

## <a name="output-quality"></a>Qualità dell'output

È possibile specificare la qualità di output del DSP del ricampionatore audio chiamando [**IWMResamplerProps:: SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) o impostando la proprietà [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY**](mfpkey-wmresamp-filterquality.md) . Se non si specifica la qualità dell'output, il DSP del ricampionatore audio utilizza un valore di qualità predefinito pari a 30.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
