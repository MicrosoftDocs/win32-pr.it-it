---
description: Il codificatore audio MPEG-2 Microsoft Media Foundation è una trasformazione Media Foundation che codifica audio mono o stereo in MPEG-1 audio (ISO/IEC 11172-3) o MPEG-2 audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificatore audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880066"
---
# <a name="mpeg-2-audio-encoder"></a>Codificatore audio MPEG-2

Il codificatore audio MPEG-2 Microsoft Media Foundation è una [trasformazione Media Foundation](media-foundation-transforms.md) che codifica audio mono o stereo in MPEG-1 audio (ISO/IEC 11172-3) o MPEG-2 audio (ISO/IEC 13818-3).

Il codificatore supporta l'audio di livello 1 e 2. Non supporta l'audio MPEG-Layer 3 (MP3). Per MPEG-2, il codificatore supporta la porzione low Sampling frequenze (LSF) dell'audio MPEG-2. Non supporta le estensioni multicanale. Il MFT restituisce un flusso di formato elementare MPEG. Non è in grado di generare flussi elementari, flussi di programma o flussi di trasporto in pacchetto.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del codificatore audio MEPG-2 è **CLSID \_ CMPEG2AudioEncoderMFT**, definito nel file di intestazione wmcodecdsp. h.

## <a name="output-types"></a>Tipi di output

Il tipo di output deve essere impostato per primo, prima del tipo di input. Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
<th>Osservazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principale.</td>
<td>Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sottotipo audio.</td>
<td>Obbligatorio. Deve essere <strong>MFAudioFormat_MPEG</strong>. Questo sottotipo viene usato sia per audio MPEG-1 che MPEG-2.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Campioni al secondo.</td>
<td>Obbligatorio. Per MPEG-1 e MPEG-2 sono supportati i valori seguenti:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
Per MPEG-2 LSF sono inoltre supportati i valori seguenti: <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali.</td>
<td>Obbligatorio. Deve essere 1 (mono) o 2 (stereo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Se impostato, il valore deve essere 0x3 per i canali stereo (front left e Right) o 0x4 per mono (canale front-end).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocità in bit del flusso MPEG codificato, in byte al secondo.</td>
<td>facoltativo.<br/> Le specifiche ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definiscono diverse velocità in bit, a seconda della frequenza di campionamento, del numero di canali e del livello audio (1 o 2). <br/> Per impostazione predefinita, l'audio del codificatore è di livello 2. Se l'attributo <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> non è impostato, il codificatore usa le seguenti velocità in bit predefinite:<br/>
<ul>
<li>MPEG-1 stereo: 224.000 bit al secondo (BPS) = 28.000 byte al secondo.</li>
<li>MPEG-1 mono: 192.000 bps = 24.000 byte al secondo.</li>
<li>MPEG-2 LSF, mono o stereo: 160.000 bps = 20.000 byte al secondo.</li>
</ul>
Questo attributo può essere impostato su altri valori. Se il valore non è valido in base alle specifiche MPEG, il MFT rifiuterà il tipo di supporto.<br/> È anche possibile impostare la velocità in bit usando l'interfaccia <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> . Per ulteriori informazioni, vedere la sezione Osservazioni.<br/></td>
</tr>
</tbody>
</table>



 

Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.

## <a name="input-types"></a>Tipi di input

Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di input.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
<th>Osservazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principale.</td>
<td>Obbligatorio. Deve essere <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Sottotipo audio.</td>
<td>Obbligatorio. Deve essere <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Numero di bit per esempio audio.</td>
<td>Obbligatorio. Il valore deve essere 16 se il sottotipo è <strong>MFAudioFormat_PCM</strong>, oppure 32 se il sottotipo è <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Campioni al secondo.</td>
<td>Obbligatorio. Deve corrispondere al tipo di output.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali.</td>
<td>Obbligatorio. Deve corrispondere al tipo di output.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Allineamento del blocco in byte.</td>
<td>Obbligatorio. Calcolare il valore come segue:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: numero di canali × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: numero di canali × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocità in bit del flusso AC3 codificato, in byte al secondo.</td>
<td>Obbligatorio. È necessario che l'allineamento a blocchi sia uguale a × campioni al secondo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Se impostato, il valore deve corrispondere al tipo di output.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Numero di bit validi di dati audio in ogni esempio audio.</td>
<td>facoltativo. Se impostato, il valore deve essere identico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

Il codificatore non supporta la conversione della frequenza di campionamento o la conversione stereo/mono. Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.

## <a name="codec-properties"></a>Proprietà codec

Il codificatore supporta le seguenti proprietà tramite l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .



| Proprietà                                                                                | Descrizione                                                                                      | Valore predefinito                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codecapis \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Specifica la velocità in bit codificata media, in bit al secondo.                                      | Come descritto per l'attributo [MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di supporto di output.                      |
| [Codecapis \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Specifica la modalità di codifica audio MPEG.                                                          | Stereo per audio a 2 canali o canale singolo per audio a 1 canale.<br/> Per l'audio a 2 canali, il codificatore supporta anche il Dual Channel e lo stereo misto.<br/> |
| [Codecapis \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Specifica se impostare il bit di copyright nel flusso audio MPEG.                             | Nessun copyright.                                                                                                                                                          |
| [Codecapis \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Specifica il tipo di filtro di deenfasi da usare quando il flusso codificato viene decodificato. | Non è stata specificata alcuna enfasi.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame.                    | Un checksum CRC viene scritto nel flusso di bit.                                                                                                                           |
| [Codecapis \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Specifica il livello audio MPEG.                                                                  | Audio di livello 2.                                                                                                                                                         |
| [Codecapis \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Specifica se impostare per il bit originale nel flusso audio MPEG.                          | Il bit "originale" è disattivato.                                                                                                                                                 |
| [Codecapis \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Specifica se impostare per il bit utente privato nel flusso audio MPEG.                      | Il bit utente privato è disattivato.                                                                                                                                               |



 

Per ottenere un puntatore all'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in MFT.

Il MFT implementa i metodi di [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) seguenti:

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Tutti gli altri metodi [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) restituiscono **E \_ NOTIMPL**.

## <a name="remarks"></a>Commenti

Ogni frame audio MPEG contiene esempi audio 384 (livello 1) o 1152 (livello 2) per canale. Ogni buffer di input per il codificatore può tuttavia contenere un numero qualsiasi di campioni PCM. La dimensione di ogni buffer di input deve essere un multiplo dell'allineamento del blocco. Il codificatore memorizza nella cache gli esempi di input fino a quando non è sufficiente per un frame audio MPEG.

Ogni buffer di output contiene un frame MPEG non elaborato. Le dimensioni di ogni buffer di output dipendono dalla velocità in bit e dalla frequenza di campionamento.

### <a name="configuring-the-encoder"></a>Configurazione del codificatore

Per modificare le impostazioni predefinite del codificatore, seguire questa procedura:

1.  Creare un'istanza del codificatore MFT.
2.  Chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco dei tipi di output preferiti. Il codificatore enumera tutte le frequenze di campionamento sia per mono che per stereo. Selezionare uno di questi tipi di supporti, in base alla frequenza di campionamento e al numero di canali. L'attributo [MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) indica la velocità in bit predefinita, in byte al secondo.
3.  Facoltativo: è possibile eseguire l'override della velocità in bit predefinita impostando un nuovo valore per i [ \_ byte media audio MF mt \_ \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di supporto di output. Le velocità in bit valide dipendono dalla frequenza di campionamento, dal numero di canali e dal livello audio.
    > [!Note]  
    > A questo punto del processo di configurazione, per impostazione predefinita il codificatore corrisponde all'audio di livello 2 e accetterà solo le velocità in bit di livello 2. Sarà possibile passare il codificatore al livello 1 in un passaggio successivo. vedere il passaggio 7. In tal caso, lasciare la velocità in bit predefinita per ora; è possibile modificarlo di nuovo nel passaggio 8.

     

4.  Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di output. Se si imposta un valore personalizzato per [i \_ \_ byte media audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) e la MFT rifiuta il tipo di supporto di output, è probabile che sia stata specificata una velocità in bit non valida.
5.  Chiamare [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) per enumerare il tipo di supporto di input. Poiché la frequenza di campionamento e il numero di canali devono essere identici a quelli del tipo di output, vengono enumerate solo due opzioni: input PCM a virgola mobile a 32 bit e input PCM a 16 bit. Selezionare una di queste.
6.  Chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di supporto di input.
7.  Facoltativo: per codificare l'audio di livello 1, impostare la proprietà [CODEcapis \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) su **eAVEncMPALayer \_ 1**.
8.  Facoltativo: per modificare la velocità in bit, impostare la proprietà [CODEcapis \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . La velocità in bit deve essere una delle frequenze di bit valide elencate nelle specifiche MPEG-1 o MPEG-2 LSF. In alternativa, è possibile chiamare [**ICodecAPI:: GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) per ottenere un elenco di velocità in bit valide, in base alle impostazioni correnti.
9.  Facoltativo: con audio a 2 canali, è possibile impostare la proprietà [CODEcapis \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) per modificare la modalità di codifica in Dual Channel o joint stereo. È possibile chiamare [**ICodecAPI:: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) per ottenere le opzioni valide. Per l'audio a 1 canale, l'unica opzione è mono.
10. Facoltativo: impostare le altre proprietà [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) elencate in precedenza.

È importante seguire l'ordine di questi passaggi. In particolare, impostare il tipo di supporto di output prima di modificare le proprietà [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Inoltre, è necessario impostare le proprietà di **ICodecAPI** prima che il MFT riceva il primo campione di input. Dopo la ricezione dell'input da parte di MFT, le proprietà del codec sono di sola lettura e [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) restituisce il valore **S \_ false**.

### <a name="supported-bit-rates"></a>Velocità in bit supportate

Il codificatore supporta le seguenti velocità in bit.



MPEG-1

MPEG-2

Livello 1

Livello 2

Livello 1

Livello 2

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* Solo mono  
\*\* Solo stereo  
</dl>

### <a name="example-media-types"></a>Tipi di supporti di esempio

Di seguito è riportato un esempio dei tipi di supporto necessari per codificare un PCM a 16 bit di tipo Integer, 48-kHz audio stereo alla velocità in bit predefinita.

Tipo di supporto di output:

| Attributo                                                                           | Valore                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [\_ \_ tipo principale MF \_ mt](mf-mt-major-type-attribute.md)                               | **\_Audio MFMediaType**  |
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                                      | **\_MPEG MFAudioFormat** |
| [\_ \_ campioni audio MF \_ mt \_ al \_ secondo](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [numero \_ di \_ \_ canali audio MF mt \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

Tipo di supporto di input:

| Attributo                                                                                | Valore                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_ \_ tipo principale MF \_ mt](mf-mt-major-type-attribute.md)                                    | **\_Audio MFMediaType** |
| [sottotipo MF \_ mt \_](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [\_ \_ bit audio MF \_ mt \_ per \_ campione](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_ \_ campioni audio MF \_ mt \_ al \_ secondo](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [numero \_ di \_ \_ canali audio MF mt \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_ \_ \_ allineamento blocchi audio MF \_ mt](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
