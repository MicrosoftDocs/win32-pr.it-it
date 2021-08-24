---
description: Proprietà API codec
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Proprietà API codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91346b6595944b8e95da5e9e43023052119e49a8b88809fce08b6fca780beba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792911"
---
# <a name="codec-api-properties"></a>Proprietà API codec

-   [Proprietà audio comuni](#common-audio-properties)
-   [Proprietà comuni del decodificatore](#common-decoder-properties)
-   [Proprietà comuni del codificatore](#common-encoder-properties)
-   [Proprietà decodificatore video](#video-decoder-properties)
-   [Proprietà decodificatore audio](#audio-decoder-properties)
-   [Proprietà del codificatore video](#video-encoder-properties)
-   [Proprietà del codificatore audio](#audio-encoder-properties)
-   [Proprietà del codificatore video MPEG](#mpeg-video-encoder-properties)
-   [Proprietà del codificatore audio MPEG](#mpeg-audio-encoder-properties)
-   [Proprietà del decodificatore audio digitale Dolby](#dolby-digital-audio-decoder-properties)
-   [Proprietà del codificatore audio digitale Dolby](#dolby-digital-audio-encoder-properties)
-   [Proprietà DSP (Digital Signal Processing)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Proprietà audio comuni

Queste proprietà si applicano sia ai codificatori audio che ai decodificatori audio.



| Proprietà                                                      | Descrizione                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Ottiene la configurazione del parlante per i canali audio nel flusso di bit audio. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Ottiene il numero di canali nel flusso di bit audio.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Ottiene la frequenza di campionamento del flusso di bit audio, in campioni al secondo.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Specifica se l'audio è codificato in Dolby Surround.                      |



 

### <a name="common-decoder-properties"></a>Proprietà comuni del decodificatore

Queste proprietà si applicano sia ai decodificatori audio che ai decodificatori video.



| Proprietà                                                            | Descrizione                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Specifica il formato di input corrente per il decodificatore.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Ottiene la velocità in bit media corrente del decodificatore.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Specifica il formato di output per il decodificatore.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Specifica la classe Multimedia Class Scheduler Service (MMCSS) per il thread di decodifica. |



 

### <a name="common-encoder-properties"></a>Proprietà comuni del codificatore

Queste proprietà si applicano sia ai codificatori audio che ai codificatori video.



| Proprietà                                                                          | Descrizione                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Specifica lo schema di codifica.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Specifica il livello iniziale del buffer di codifica.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Specifica il livello finale del buffer di codifica alla fine del processo di codifica.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Specifica le dimensioni del buffer utilizzato durante la codifica.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Specifica il formato di destinazione per un codificatore.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una bassa latenza di decodifica. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Specifica la velocità in bit massima.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Specifica la velocità in bit media.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Specifica l'intervallo di tempo a cui si applica la velocità in bit media.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Specifica la velocità in bit minima.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Specifica il numero di passaggi di codifica supportati dal codificatore.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Arresta il passaggio di codifica corrente o verifica se il passaggio di codifica corrente è l'ultimo.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Avvia il primo passaggio di codifica.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Specifica il livello di qualità per la codifica.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Specifica il compromesso tra qualità e velocità della codifica.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Specifica la modalità di controllo della frequenza.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Specifica se il codificatore rimuove gruppi parziali di immagini (GOP) alla fine del flusso.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Specifica il tipo di flusso di output prodotto da un multiplexer.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Specifica il numero di passaggi di codifica completati.                                                              |



 

### <a name="video-decoder-properties"></a>Proprietà decodificatore video



| Proprietà                                                                                | Descrizione                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Abilita o disabilita l'accelerazione hardware per la decodifica video H.264.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Abilita o disabilita l'accelerazione hardware per la decodifica video MPEG-2.            |
| [**AVDecVideoAcceleration \_ VC1**](avdecvideoacceleration-vc1-property.md)              | Abilita o disabilita l'accelerazione hardware per la decodifica video VC-1.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Specifica se il decodificatore elimina i fotogrammi intra con fotogrammi di riferimento mancanti. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Ottiene o imposta la velocità di decodifica video.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Ottiene le dimensioni dell'immagine decodificata, in pixel.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Specifica la modalità di interlacciazione del flusso video decodificato.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Specifica le proporzioni pixel del flusso video decodificato.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Specifica la modalità deinterlace software del decodificatore.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Specifica il livello di risparmio energia.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Abilita o disabilita la modalità di generazione delle anteprime.                                  |



 

### <a name="audio-decoder-properties"></a>Proprietà decodificatore audio



| Proprietà                                                                        | Descrizione                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Specifica se un decodificatore AAC usa equazioni downmix stereo MPEG-2/MPEG-4 standard o usa un downmix non standard. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Specifica la modalità di riproduzione dell'audio doppio mono da parte del decodificatore.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Abilita o disabilita il controllo di intervallo dinamico in un decodificatore AAC.                                                           |



 

### <a name="video-encoder-properties"></a>Proprietà del codificatore video



| Proprietà                                                                                        | Descrizione                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Specifica il sistema video del contenuto di origine.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Restituisce il numero di fotogrammi video codificati.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Restituisce la frequenza media dei fotogrammi del contenuto video.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Restituisce il numero di fotogrammi video ricevuti dal codificatore.                                                         |
| [**AVEncVideoCBRMotionTradeoff**](avencvideocbrmotiontradeoff-property.md)                     | Specifica il compromesso tra il movimento e le immagini fisse.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Specifica le dimensioni delle unità di accesso video.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Specifica il campo da visualizzare per primo.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Specifica le dimensioni del flusso video quando viene decodificato.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Specifica la larghezza e l'altezza del video codificato, se il video viene ritagliato.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Specifica gli angoli sinistro e superiore del rettangolo di ritaglio, se il video è ritagliato.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Inverte l'ordine dei campi interlacciati nel video di origine.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Specifica se i fotogrammi di input sono progressivi o interlacciati.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Specifica il valore del flag drop-frame nell'intestazione GOP.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Specifica il numero di frame iniziale nell'intestazione GOP.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Specifica il numero di ora iniziale nell'intestazione GOP.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Specifica il numero di minuti iniziale nell'intestazione GOP.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Specifica il secondo numero iniziale nell'intestazione GOP.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Specifica la risoluzione della croma del video di input.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Specifica il siting di chroma per il video di input.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Specifica le condizioni di illuminazione per la visualizzazione del video di input.                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | Specifica l'intervallo nominale per il video di input.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Specifica i colori primari per il video di input.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Specifica la funzione di conversione da RGB a R'G'B' per il video di input                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Specifica la matrice di conversione dallo spazio colori Y'Cb'Cr' allo spazio colore R'G'B' per il video di input.         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | Specifica se il codificatore esegue telecine inverso.                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | Imposta la soglia alla quale il codificatore considera ridondante un campo video.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Specifica il numero massimo di fotogrammi tra fotogrammi chiave.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Specifica il numero di campi da codificare.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Specifica il numero di campi da ignorare durante la codifica.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Specifica la risoluzione chroma del video codificato.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Specifica il siting di chroma per il video codificato.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Specifica le condizioni di illuminazione per la visualizzazione del video codificato.                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | Specifica l'intervallo nominale per il video codificato.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Specifica i colori primari per il video codificato.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Specifica la funzione di conversione da RGB a R'G'B' per il video codificato.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Specifica la matrice di conversione dallo spazio colori Y'Cb'Cr' allo spazio colore R'G'B' per il video codificato.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Specifica la frequenza dei fotogrammi nel flusso di output del codificatore, in fotogrammi al secondo.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Specifica se il codificatore converte la frequenza dei fotogrammi quando la frequenza dei fotogrammi di output non corrisponde alla frequenza dei fotogrammi di input. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Specifica il modo in cui il codificatore interlaccia il video di output.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Specifica le proporzioni in pixel.                                                                                     |
| [**AVEncVideoSourceContent**](avencvideosourcefilmcontent-property.md)                     | Specifica se l'origine originale del video di input è film o video.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Specifica se il video è monocromatico (bianco e nero) o contiene colore.                                        |



 

### <a name="audio-encoder-properties"></a>Proprietà del codificatore audio



| Proprietà                                                                        | Descrizione                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Specifica se il contenuto audio contiene musica o voce.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Specifica il numero di campioni audio da codificare.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Specifica il numero di campioni audio da ignorare per il codificatore.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Specifica quale canale audio viene mappato al canale *N* nel flusso audio codificato. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Specifica la velocità in bit media del flusso audio codificato.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Restituisce i bit medi al secondo dell'audio codificato.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Restituisce il livello di volume medio del contenuto audio.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Restituisce il livello di volume più alto presente nel contenuto audio.             |



 

### <a name="mpeg-video-encoder-properties"></a>Proprietà del codificatore video MPEG



| Proprietà                                                                                    | Descrizione                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Specifica se il codificatore aggiunge un codice di fine sequenza alla fine del flusso.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Specifica il numero predefinito di fotogrammi B consecutivi tra i frame I e P.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Specifica se il codificatore produce campi codificati o fotogrammi codificati.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Specifica se il codificatore genera intestazioni di estensione per la visualizzazione di immagini.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Specifica se il codificatore genera intestazioni di estensione immagine.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Specifica se il codificatore genera intestazioni di estensione di visualizzazione della sequenza.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Specifica se il codificatore genera intestazioni di estensione della sequenza.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Specifica se il codificatore genera intestazioni di estensione scalabili in sequenza.         |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                         | Specifica se il codificatore produce GOP aperti o GOP chiusi.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Specifica il numero di GOP tra le intestazioni di sequenza.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Specifica il numero massimo di immagini da un'intestazione GOP all'intestazione GOP successiva. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Specifica la precisione dei coefficienti DC.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Specifica la tabella VLC (Variable-Length Coding) da usare per la codifica entropia.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Specifica il livello MPEG-2.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Specifica il profilo MPEG-2.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Specifica se la scala del quantizer è lineare o non lineare.                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | Specifica la matrice di quantizzazione chroma per i macroblock all'interno.                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Specifica la matrice di quantizzazione chroma per macroblock non intra.                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Specifica la matrice di quantizzazione luma per i macroblock all'interno.                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Specifica la matrice di quantizzazione luma per macroblock non intra.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Specifica il modello di analisi macroblock.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Specifica il comportamento del codificatore quando rileva una nuova scena.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Specifica se il codificatore usa vettori di movimento di mascheramento.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>Proprietà del codificatore audio MPEG



| Proprietà                                                                                  | Descrizione                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Specifica la modalità di codifica audio MPEG-1.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Specifica l'impostazione predefinita per il bit di copyright.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Specifica il tipo di filtro di rimozione dell'enfasi da usare durante la decodifica.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Specifica il livello audio MPEG.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Specifica l'impostazione predefinita per il bit originale.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Imposta il valore del bit dell'utente privato.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Proprietà del decodificatore audio digitale Dolby



| Proprietà                                                                      | Descrizione                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecdDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Specifica il taglio di alto livello quando il decodificatore esegue il controllo dinamico dell'intervallo.  |
| [**AVDecdDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Specifica la priorità di basso livello quando il decodificatore esegue il controllo dinamico dell'intervallo. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Specifica la modalità di controllo della compressione.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Proprietà del codificatore audio digitale Dolby



| Proprietà                                                                                        | Descrizione                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtodConverterType**](avencddatodconvertertype-property.md)                           | Specifica il tipo di conversione da analogico a digitale (A/D).                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Specifica il livello di downmix centrale.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Specifica se ai canali di input principali viene applicato un filtro pass basso.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Specifica il flag di copyright.                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Specifica se viene applicato un filtro pass elevato di blocco del controller di dominio.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Specifica il livello di normalizzazione del dialogo.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Specifica se la de-enfasi digitale.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Specifica il profilo di controllo dell'intervallo dinamico.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Specifica la modalità dell'altoparlante.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Specifica se al canale con effetto a bassa frequenza (LFE) viene applicato un filtro pass basso. |
| [**AVEncDDLoRoCenterMixLvl \_ x10**](avencddlorocentermixlvl-x10-property.md)                    | Specifica lo spostamento del livello applicato al canale centrale per il downmixing Lo/Ro.     |
| [**AVEncDDLoRoSurroundMixLvl \_ x10**](avencddlorosurroundmixlvl-x10-property.md)                | Specifica lo spostamento del livello applicato ai canali surround per il downmixing lo/ro.  |
| [**AVEncDDLtRtCenterMixLvl \_ x10**](avencddltrtcentermixlvl-x10-property.md)                    | Specifica lo spostamento del livello applicato al canale centrale per il downmixing Lt/Rt.     |
| [**AVEncDDLtRtSurroundMixLvl \_ x10**](avencddltrtsurroundmixlvl-x10-property.md)                | Specifica lo spostamento del livello applicato ai canali surround per il downmixing Lt/Rt.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Specifica il flag bitstream originale.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Specifica la modalità downmix stereo preferita.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Specifica il flag delle informazioni di produzione audio.                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Specifica il livello di combinazione.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Specifica il tipo di stanza.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Specifica l'impostazione di protezione dell'overmodulation RF.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Specifica il servizio audio.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Specifica se i canali surround vengono attenuati prima della codifica.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Specifica se ai canali surround viene applicato uno spostamento di fase di 90 gradi.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Specifica il livello di combinazione Racchiude verso il basso.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Specifica se il flusso audio è codificato in Surround EX.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Proprietà DSP (Digital Signal Processing)



| Proprietà                                                                | Descrizione                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | Abilita o disabilita l'equalizzazione della sonorità |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Abilita o disabilita il riempimento della voce          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API codec](codec-api-reference.md)
</dt> </dl>

 

 



