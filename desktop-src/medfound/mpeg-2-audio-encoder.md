---
description: Il codificatore audio Microsoft Media Foundation MPEG-2 è una trasformazione Media Foundation che codifica audio mono o stereo in audio MPEG-1 (ISO/IEC 11172-3) o audio MPEG-2 (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificatore audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 935b6438c79e9bf78a230f707f8930f859c3fa491dab0326208d5cf79b53f474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240010"
---
# <a name="mpeg-2-audio-encoder"></a>Codificatore audio MPEG-2

Il codificatore audio mpeg-2 Microsoft Media Foundation è una trasformazione [Media Foundation che](media-foundation-transforms.md) codifica audio mono o stereo in audio MPEG-1 (ISO/IEC 11172-3) o audio MPEG-2 (ISO/IEC 13818-3).

Il codificatore supporta audio di livello 1 e di livello 2. Non supporta audio MPEG-Layer 3 (MP3). Per MPEG-2, il codificatore supporta la parte low sampling frequencies (LSF) dell'audio MPEG-2. Non supporta le estensioni multicanale. MFT restituisce un flusso elementare MPEG. Non può generare flussi elementari in pacchetto, flussi di programma o flussi di trasporto.

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) del codificatore audio MEPG-2 è **CLSID \_ CMPEG2AudioEncoderMFT,** definito nel file di intestazione wmcodecdsp.h.

## <a name="output-types"></a>Tipi di output

Il tipo di output deve essere impostato prima del tipo di input. Nella tabella seguente sono elencati gli attributi obbligatori e facoltativi per il tipo di supporto di output.



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
<td>Obbligatorio. Deve essere <strong>MFAudioFormat_MPEG</strong>. Questo sottotipo viene usato per l'audio MPEG-1 e MPEG-2.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Esempi al secondo.</td>
<td>Obbligatorio. I valori seguenti sono supportati sia per MPEG-1 che per MPEG-2:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
Per MPEG-2 LSF sono supportati anche i valori seguenti: <br/>
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
<td>facoltativo. Se impostato, il valore deve essere 0x3 per stereo (canali anteriore sinistro e destro) o per 0x4 mono (canale anteriore centrale).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocità in bit del flusso MPEG codificato, in byte al secondo.</td>
<td>facoltativo.<br/> Le specifiche ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definiscono diverse velocità in bit, a seconda della frequenza di campionamento, del numero di canali e del livello audio (1 o 2). <br/> Per impostazione predefinita, il codificatore è audio di livello 2. Se <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">l'MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> non è impostato, il codificatore usa le velocità in bit predefinite seguenti:<br/>
<ul>
<li>Stereo MPEG-1: 224.000 bit al secondo (bps) = 28.000 byte al secondo.</li>
<li>MPEG-1 mono: 192.000 bps = 24.000 byte al secondo.</li>
<li>MPEG-2 LSF, mono o stereo: 160.000 bps = 20.000 byte al secondo.</li>
</ul>
Questo attributo può essere impostato su altri valori. Se il valore non è valido in base alle specifiche MPEG, il MFT rifiuterà il tipo di supporto.<br/> È anche possibile impostare la velocità in bit usando <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>l'interfaccia ICodecAPI.</strong></a> Per ulteriori informazioni, vedere la sezione Osservazioni.<br/></td>
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
<td>Numero di bit per campione audio.</td>
<td>Obbligatorio. Il valore deve essere 16 se il sottotipo è <strong>MFAudioFormat_PCM</strong>o 32 se il sottotipo <strong>è MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Esempi al secondo.</td>
<td>Obbligatorio. Deve corrispondere al tipo di output.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Numero di canali.</td>
<td>Obbligatorio. Deve corrispondere al tipo di output.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Allineamento dei blocchi, in byte.</td>
<td>Obbligatorio. Calcolare il valore come segue:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: numero di canali × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: numero di canali × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Velocità in bit del flusso AC3 codificato, in byte al secondo.</td>
<td>Obbligatorio. Deve essere uguale all'allineamento × al secondo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Specifica l'assegnazione dei canali audio alle posizioni degli altoparlanti.</td>
<td>facoltativo. Se impostato, il valore deve corrispondere al tipo di output.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Numero di bit validi di dati audio in ogni campione audio.</td>
<td>facoltativo. Se impostato, il valore deve essere identico <a href="mf-mt-audio-bits-per-sample-attribute.md">a</a>MF_MT_AUDIO_BITS_PER_SAMPLE .</td>
</tr>
</tbody>
</table>



 

Il codificatore non supporta la conversione della frequenza di campionamento o la conversione stereo/mono. Se gli attributi facoltativi non sono impostati, il codificatore li aggiunge al tipo di supporto dopo l'impostazione del tipo.

## <a name="codec-properties"></a>Proprietà codec

Il codificatore supporta le proprietà seguenti tramite [**l'interfaccia ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)



| Proprietà                                                                                | Descrizione                                                                                      | Valore predefinito                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Specifica la velocità in bit codificata media, in bit al secondo.                                      | Come descritto per [l'attributo \_ MF MT \_ AUDIO \_ AVG \_ BYTES PER \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di supporto di output.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Specifica la modalità di codifica audio MPEG.                                                          | Stereo per audio a 2 canali o canale singolo per audio a 1 canale.<br/> Per l'audio a 2 canali, il codificatore supporta anche il doppio canale e lo stereo congiunto.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Specifica se impostare il bit di copyright nel flusso audio MPEG.                             | Nessun copyright.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Specifica il tipo di filtro di de-enfasi che deve essere usato quando il flusso codificato viene decodificato. | Nessuna enfasi specificata.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame.                    | Un checksum CRC viene scritto nel flusso di bit.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Specifica il livello audio MPEG.                                                                  | Audio di livello 2.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Specifica se impostare per il bit originale nel flusso audio MPEG.                          | Il bit "Original" è disattivato.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Specifica se impostare per il bit utente privato nel flusso audio MPEG.                      | Il bit dell'utente privato è disattivato.                                                                                                                                               |



 

Per ottenere un puntatore [**all'interfaccia ICodecAPI,**](/windows/win32/api/strmif/nn-strmif-icodecapi) chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su MFT.

MFT implementa i metodi [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) seguenti:

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**Getvalue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**IsModifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Tutti gli [**altri metodi ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) restituiscono **E \_ NOTIMPL.**

## <a name="remarks"></a>Commenti

Ogni fotogramma audio MPEG contiene campioni audio 384 (livello 1) o 1152 (livello 2) per canale. Tuttavia, ogni buffer di input per il codificatore può contenere un numero qualsiasi di campioni PCM. La dimensione di ogni buffer di input deve essere un multiplo dell'allineamento del blocco. Il codificatore memorizza nella cache i campioni di input fino a quando non è sufficiente per un frame audio MPEG.

Ogni buffer di output contiene un frame MPEG non elaborato. Le dimensioni di ogni buffer di output dipendono dalla velocità in bit e dalla frequenza di campionamento.

### <a name="configuring-the-encoder"></a>Configurazione del codificatore

Per modificare le impostazioni predefinite nel codificatore, seguire questa procedura:

1.  Creare un'istanza del codificatore MFT.
2.  Chiamare [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) per ottenere l'elenco dei tipi di output preferiti. Il codificatore enumera tutte le frequenze di campionamento per mono e stereo. Selezionare uno di questi tipi di supporti, in base alla frequenza di campionamento e al numero di canali. [L'attributo \_ MF MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) indica la velocità in bit predefinita, in byte al secondo.
3.  Facoltativo: è possibile eseguire l'override della velocità in bit predefinita impostando un nuovo valore per [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) nel tipo di supporto di output. Le velocità in bit valide dipendono dalla frequenza di campionamento, dal numero di canali e dal livello audio.
    > [!Note]  
    > A questo punto del processo di configurazione, il codificatore usa per impostazione predefinita l'audio di livello 2 e accetta solo velocità in bit di livello 2. Sarà possibile passare il codificatore al livello 1 in un passaggio successivo (vedere il passaggio 7). In tal caso, lasciare la velocità in bit predefinita per il momento. è possibile modificarlo nuovamente nel passaggio 8.

     

4.  Chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di output. Se si imposta un valore personalizzato per [MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) e MFT rifiuta il tipo di supporto di output, è probabile che sia stata specificata una velocità in bit non valida.
5.  Chiamare [**IMFTransform::GetInputAvailableType per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) enumerare il tipo di supporto di input. Poiché la frequenza di campionamento e il numero di canali devono essere identici al tipo di output, vengono enumerate solo due opzioni: input PCM a virgola mobile a 32 bit e input PCM di tipo Integer a 16 bit. Selezionare una di queste opzioni.
6.  Chiamare [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il tipo di supporto di input.
7.  Facoltativo: per codificare l'audio di livello 1, impostare la proprietà [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) su **eAVEncMPALayer \_ 1.**
8.  Facoltativo: per modificare la velocità in bit, impostare la [proprietà CODECAPI \_ AVEncCommonMeanBitRate.](../directshow/avenccommonmeanbitrate-property.md) La velocità in bit deve essere una delle velocità in bit valide elencate nelle specifiche LSF MPEG-1 o MPEG-2. In alternativa, è possibile chiamare [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) per ottenere un elenco di velocità in bit valide, in base alle impostazioni correnti.
9.  Facoltativo: con l'audio a 2 canali, è possibile impostare la proprietà [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) per impostare la modalità di codifica su doppio canale o stereo congiunto. È possibile chiamare [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) per ottenere le opzioni valide. Per l'audio a 1 canale, l'unica opzione è mono.
10. Facoltativo: impostare una delle altre proprietà [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) elencate in precedenza.

È importante seguire l'ordine di questi passaggi. In particolare, impostare il tipo di supporto di output prima di modificare le [**proprietà ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi) Inoltre, è necessario impostare **le proprietà ICodecAPI** prima che MFT riceva il primo esempio di input. Dopo che MFT ha ricevuto l'input, le proprietà del codec sono di sola lettura e [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) restituisce il **valore S \_ FALSE.**

### <a name="supported-bit-rates"></a>Velocità in bit supportate

Il codificatore supporta le velocità in bit seguenti.



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



 

<dl> \* Solo Mono  
\*\* Solo stereo  
</dl>

### <a name="example-media-types"></a>Tipi di supporti di esempio

Di seguito è riportato un esempio dei tipi di supporti necessari per codificare l'audio stereo a 48 kHz e l'intero PCM a 16 bit alla velocità in bit predefinita.

Tipo di supporto di output:

| Attributo                                                                           | Valore                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                               | **MFMediaType \_ Audio**  |
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [CANALI \_ NUM AUDIO MT MF \_ \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

Tipo di supporto di input:

| Attributo                                                                                | Valore                  |
|------------------------------------------------------------------------------------------|------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                                    | **MFMediaType \_ Audio** |
| [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [CANALI \_ NUM AUDIO MT MF \_ \_ \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
