---
description: Proprietà dell'API codec
ms.assetid: 5d527af7-07cf-42e2-99bb-d56c856cc1bc
title: Proprietà dell'API codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06269591c8ddf087b83146ed72a62f4565b8340a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481188"
---
# <a name="codec-api-properties"></a>Proprietà dell'API codec

-   [Proprietà audio comuni](#common-audio-properties)
-   [Proprietà del decodificatore comuni](#common-decoder-properties)
-   [Proprietà del codificatore comune](#common-encoder-properties)
-   [Proprietà del decodificatore video](#video-decoder-properties)
-   [Proprietà del decodificatore audio](#audio-decoder-properties)
-   [Proprietà del codificatore video](#video-encoder-properties)
-   [Proprietà del codificatore audio](#audio-encoder-properties)
-   [Proprietà del codificatore video MPEG](#mpeg-video-encoder-properties)
-   [Proprietà del codificatore audio MPEG](#mpeg-audio-encoder-properties)
-   [Proprietà del decodificatore Dolby Digital audio](#dolby-digital-audio-decoder-properties)
-   [Proprietà del codificatore audio Dolby Digital](#dolby-digital-audio-encoder-properties)
-   [Proprietà di elaborazione dei segnali digitali (DSP)](#digital-signal-processing-dsp-properties)

### <a name="common-audio-properties"></a>Proprietà audio comuni

Queste proprietà si applicano sia ai codificatori audio sia ai decodificatori audio.



| Proprietà                                                      | Descrizione                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md) | Ottiene la configurazione dell'altoparlante per i canali audio nel flusso di bit audio. |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)   | Ottiene il numero di canali nel flusso di bit audio.                           |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)       | Ottiene la frequenza di campionamento del flusso di bit audio, in campioni al secondo.          |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)         | Specifica se l'audio è codificato in Dolby surround.                      |



 

### <a name="common-decoder-properties"></a>Proprietà del decodificatore comuni

Queste proprietà si applicano sia a decodificatori audio che a decodificatori video.



| Proprietà                                                            | Descrizione                                                                             |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)   | Specifica il formato di input corrente per il decodificatore.                                     |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)            | Ottiene la velocità in bit media corrente del decodificatore.                                          |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) | Specifica il formato di output per il decodificatore.                                            |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                      | Specifica la classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il thread di decodifica. |



 

### <a name="common-encoder-properties"></a>Proprietà del codificatore comune

Queste proprietà si applicano sia ai codificatori audio che ai codificatori video.



| Proprietà                                                                          | Descrizione                                                                                                     |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                 | Specifica lo schema di codifica.                                                                                  |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)             | Specifica il livello iniziale del buffer di codifica.                                                             |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)           | Specifica il livello finale del buffer di codifica alla fine del processo di codifica.                            |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                   | Specifica le dimensioni del buffer utilizzato durante la codifica.                                                          |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)       | Specifica il formato di destinazione per un codificatore.                                                                     |
| [**AVEncCommonLowLatency**](avenccommonlowlatency-property.md)                   | Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una latenza di decodifica bassa. |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                   | Specifica la velocità in bit massima.                                                                                 |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                 | Specifica la velocità in bit media.                                                                                 |
| [**AVEncCommonMeanBitRateInterval**](avenccommonmeanbitrateinterval-property.md) | Specifica l'intervallo di tempo in base al quale viene applicata la velocità in bit media.                                            |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                   | Specifica la velocità in bit minima.                                                                                 |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)             | Specifica il numero di passaggi di codifica supportati dal codificatore.                                              |
| [**AVEncCommonPassEnd**](avenccommonpassend-property.md)                         | Arresta il passaggio di codifica corrente o esegue una query se il passaggio di codifica corrente è l'ultimo.                  |
| [**AVEncCommonPassStart**](avenccommonpassstart-property.md)                     | Avvia il primo passaggio di codifica.                                                                                 |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                         | Specifica il livello di qualità per la codifica.                                                                       |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)           | Specifica il compromesso tra la qualità e la velocità di codifica.                                                      |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)         | Specifica la modalità di controllo della frequenza.                                                                                |
| [**AVEncCommonRealTime**](avenccommonrealtime-property.md)                       | Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.                                      |
| [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md)     | Specifica se il codificatore ignora gruppi parziali di immagini (GOPs) alla fine del flusso.              |
| [**AVEncMuxOutputStreamType**](avencmuxoutputstreamtype.md)                      | Specifica il tipo di flusso di output prodotto da un multiplexer.                                                  |
| [**AVEncStatCommonCompletedPasses**](avencstatcommoncompletedpasses-property.md) | Specifica il numero di sessioni di codifica completate.                                                              |



 

### <a name="video-decoder-properties"></a>Proprietà del decodificatore video



| Proprietà                                                                                | Descrizione                                                                     |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Abilita o Disabilita l'accelerazione hardware per la decodifica video H. 264.             |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Abilita o Disabilita l'accelerazione hardware per la decodifica video MPEG-2.            |
| [**\_VC1 AVDecVideoAcceleration**](avdecvideoacceleration-vc1-property.md)              | Abilita o Disabilita l'accelerazione hardware per la decodifica video VC-1.              |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Specifica se il decodificatore rilascia i frame intra con frame di riferimento mancanti. |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Ottiene o imposta la velocità di decodifica dei video.                                          |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Ottiene le dimensioni in pixel dell'immagine decodificata.                                  |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)                     | Specifica il modo in cui il flusso video decodificato è interlacciato.                           |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md)               | Specifica le proporzioni in pixel del flusso video decodificato.                   |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Specifica la modalità di deinterlacciamento software del decodificatore.                              |
| [**AVDecVideoSWPowerLevel**](avdecvideoswpowerlevel-property.md)                       | Specifica il livello di risparmio energia.                                               |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Abilita o Disabilita la modalità di generazione delle anteprime.                                  |



 

### <a name="audio-decoder-properties"></a>Proprietà del decodificatore audio



| Proprietà                                                                        | Descrizione                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                     | Specifica se un decodificatore AAC USA equazioni downmix standard MPEG-2/MPEG-4 stereo oppure usa un downmix non standard. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)                       | Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.                                                   |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)     | Specifica il modo in cui il decodificatore riproduce audio mono doppio.                                                                  |
| [**AVDecHEAACDynamicRangeControl**](avdecheaacdynamicrangecontrol-property.md) | Abilita o Disabilita il controllo dinamico degli intervalli in un decodificatore AAC.                                                           |



 

### <a name="video-encoder-properties"></a>Proprietà del codificatore video



| Proprietà                                                                                        | Descrizione                                                                                                           |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                                 | Specifica il sistema video del contenuto di origine.                                                                     |
| [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md)                         | Restituisce il numero di fotogrammi video codificati.                                                                 |
| [**AVEncStatVideoOutputFrameRate**](avencstatvideooutputframerate-property.md)                 | Restituisce la frequenza media dei fotogrammi del contenuto video.                                                                  |
| [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md)                         | Restituisce il numero di fotogrammi video ricevuti dal codificatore.                                                         |
| [**AVEncVideoCBRMotionTradeoff**](avencvideocbrmotiontradeoff-property.md)                     | Specifica il compromesso tra movimento e immagini fisse.                                                               |
| [**AVEncVideoCodedVideoAccessUnitSize**](avencvideocodedvideoaccessunitsize-property.md)       | Specifica le dimensioni delle unità di accesso ai video.                                                                         |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)     | Specifica il campo che viene visualizzato per primo.                                                                             |
| [**AVEncVideoDisplayDimension**](avencvideodisplaydimension-property.md)                       | Specifica le dimensioni del flusso video quando viene decodificato.                                                            |
| [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md)                         | Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.                                         |
| [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md)                   | Specifica gli angoli sinistro e superiore del rettangolo di ridimensionamento, se il video è ritagliato.                                |
| [**AVEncVideoFieldSwap**](avencvideofieldswap-property.md)                                     | Inverte l'ordine dei campi interlacciati nel video di origine.                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)                 | Specifica se i fotogrammi di input sono progressivi o interlacciati.                                                     |
| [**AVEncVideoHeaderDropFrame**](avencvideoheaderdropframe-property.md)                         | Specifica il valore del flag drop frame nell'intestazione GOP.                                                             |
| [**AVEncVideoHeaderFrames**](avencvideoheaderframes-property.md)                               | Specifica il numero del fotogramma iniziale nell'intestazione GOP.                                                                |
| [**AVEncVideoHeaderHours**](avencvideoheaderhours-property.md)                                 | Specifica il numero dell'ora di inizio nell'intestazione GOP.                                                                 |
| [**AVEncVideoHeaderMinutes**](avencvideoheaderminutes-property.md)                             | Specifica il numero di minuti di inizio nell'intestazione GOP.                                                               |
| [**AVEncVideoHeaderSeconds**](avencvideoheaderseconds-property.md)                             | Specifica il secondo numero di inizio nell'intestazione GOP.                                                               |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)             | Specifica la risoluzione croma del video di input.                                                                   |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)           | Specifica la posizione Chroma per il video di input.                                                                      |
| [**AVEncVideoInputColorLighting**](avencvideoinputcolorlighting-property.md)                   | Specifica le condizioni di illuminazione desiderate per la visualizzazione del video di input.                                               |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)           | Specifica l'intervallo nominale per il video di input.                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)                 | Specifica le primarie di colore per il video di input.                                                                    |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md)   | Specifica la funzione di conversione da RGB a SOTTOCAMPIONATURA ' per il video di input                                                  |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)       | Specifica la matrice di conversione dallo spazio colore Cb'Cr allo spazio colore SOTTOCAMPIONATURA per il video di input.         |
| [**AVEncVideoInverseTelecineEnable**](avencvideoinversetelecineenable-property.md)             | Specifica se il codificatore esegue la telecine inversa.                                                              |
| [**AVEncVideoInverseTelecineThreshold**](avencvideoinversetelecinethreshold-property.md)       | Imposta la soglia in corrispondenza della quale il codificatore considera ridondante un campo video.                                            |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)                 | Specifica il numero massimo di frame tra fotogrammi chiave.                                                            |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                   | Specifica il numero di campi da codificare.                                                                             |
| [**AVEncVideoNoOfFieldsToSkip**](avencvideonooffieldstoskip-property.md)                       | Specifica il numero di campi da ignorare durante la codifica.                                                               |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)           | Specifica la risoluzione croma del video codificato.                                                                 |
| [**AVEncVideoOutputChromaSubsampling**](avencvideooutputchromasubsampling-property.md)         | Specifica la posizione Chroma per il video codificato.                                                                    |
| [**AVEncVideoOutputColorLighting**](avencvideooutputcolorlighting-property.md)                 | Specifica le condizioni di illuminazione desiderate per la visualizzazione del video codificato.                                             |
| [**AVEncVideoOutputColorNominalRange**](avencvideooutputcolornominalrange-property.md)         | Specifica l'intervallo nominale per il video codificato.                                                                    |
| [**AVEncVideoOutputColorPrimaries**](avencvideooutputcolorprimaries-property.md)               | Specifica le primarie di colore per il video codificato.                                                                  |
| [**AVEncVideoOutputColorTransferFunction**](avencvideooutputcolortransferfunction-property.md) | Specifica la funzione di conversione da RGB a SOTTOCAMPIONATURA ' per il video codificato.                                               |
| [**AVEncVideoOutputColorTransferMatrix**](avencvideooutputcolortransfermatrix-property.md)     | Specifica la matrice di conversione dallo spazio colore Cb'Cr allo spazio colore SOTTOCAMPIONATURA per il video codificato.       |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                         | Specifica la frequenza dei fotogrammi nel flusso di output del codificatore, in frame al secondo.                                        |
| [**AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md)     | Specifica se il codificatore converte la frequenza dei fotogrammi quando la frequenza dei fotogrammi di output non corrisponde alla frequenza dei fotogrammi di input. |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                           | Specifica il modo in cui il codificatore interlaccierà il video di output.                                                                |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                       | Specifica le proporzioni in pixel.                                                                                     |
| [**AVEncVideoSourceFilmContent**](avencvideosourcefilmcontent-property.md)                     | Specifica se l'origine originale del video di input è film o video.                                           |
| [**AVEncVideoSourceIsBW**](avencvideosourceisbw-property.md)                                   | Specifica se il video è monocromatico (nero e bianco) o contiene il colore.                                        |



 

### <a name="audio-encoder-properties"></a>Proprietà del codificatore audio



| Proprietà                                                                        | Descrizione                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**AVEncAudioDualMono**](avencaudiodualmono-property.md)                       | Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.                |
| [**AVEncAudioInputContent**](avencaudioinputcontent-property.md)               | Specifica se il contenuto audio contiene musica o voce.                        |
| [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)       | Specifica il numero di campioni audio da codificare.                                    |
| [**AVEncAudioIntervalToSkip**](avencaudiointervaltoskip-property.md)           | Specifica il numero di campioni audio che il codificatore deve ignorare.                      |
| [**AVEncAudioMapDestChannel N**](avencaudiomapdestchanneln-property.md)        | Specifica il canale audio mappato al canale *N* nel flusso audio codificato. |
| [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)                          | Specifica la velocità in bit media del flusso audio codificato.                         |
| [**AVEncStatAudioAverageBPS**](avencstataudioaveragebps-property.md)           | Restituisce il numero medio di bit al secondo dell'audio codificato.                           |
| [**AVEncStatAudioAveragePCMValue**](avencstataudioaveragepcmvalue-property.md) | Restituisce il livello medio del volume del contenuto audio.                              |
| [**AVEncStatAudioPeakPCMValue**](avencstataudiopeakpcmvalue-property.md)       | Restituisce il livello di volume più elevato presente nel contenuto audio.             |



 

### <a name="mpeg-video-encoder-properties"></a>Proprietà del codificatore video MPEG



| Proprietà                                                                                    | Descrizione                                                                          |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**AVEncMPVAddSeqEndCode**](avencmpvaddseqendcode-property.md)                             | Specifica se il codificatore aggiunge un codice di fine sequenza alla fine del flusso.     |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)               | Specifica il numero predefinito di fotogrammi B consecutivi tra I frame I e P.         |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                           | Specifica se il codificatore produce campi codificati o frame codificati.             |
| [**AVEncMPVGenerateHeaderPicDispExt**](avencmpvgenerateheaderpicdispext-property.md)       | Specifica se il codificatore genera intestazioni di estensione per la visualizzazione dell'immagine.           |
| [**AVEncMPVGenerateHeaderPicExt**](avencmpvgenerateheaderpicext-property.md)               | Specifica se il codificatore genera intestazioni di estensione per le immagini.                   |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)       | Specifica se il codificatore genera intestazioni di estensione per la visualizzazione della sequenza.          |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)               | Specifica se il codificatore genera intestazioni di estensione di sequenza.                  |
| [**AVEncMPVGenerateHeaderSeqScaleExt**](avencmpvgenerateheaderseqscaleext-property.md)     | Specifica se il codificatore genera intestazioni di estensione scalabili di sequenza.         |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                         | Specifica se il codificatore produce GOPs aperti o GOPs chiusi.                     |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                     | Specifica il numero di GOPs tra le intestazioni di sequenza.                               |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                         | Specifica il numero massimo di immagini da un'intestazione GOP alla successiva intestazione GOP. |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                       | Specifica la precisione dei coefficienti del controller di dominio.                                      |
| [**AVEncMPVIntraVLCTable**](avencmpvintravlctable-property.md)                             | Specifica la tabella di codifica a lunghezza variabile (VLC) da usare per la codifica dell'entropia.        |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                             | Specifica il livello MPEG-2.                                                          |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                         | Specifica il profilo MPEG-2.                                                        |
| [**AVEncMPVQScaleType**](avencmpvqscaletype-property.md)                                   | Specifica se la scala del quantizzatore è lineare o non lineare.                       |
| [**AVEncMPVQuantMatrixChromaIntra**](avencmpvquantmatrixchromaintra-property.md)           | Specifica la matrice di quantizzazione Chroma per intra macroblocchi.                      |
| [**AVEncMPVQuantMatrixChromaNonIntra**](avencmpvquantmatrixchromanonintra-property.md)     | Specifica la matrice di quantizzazione Chroma per macroblocchi non intra.                  |
| [**AVEncMPVQuantMatrixIntra**](avencmpvquantmatrixintra-property.md)                       | Specifica la matrice di quantizzazione Luma per intra macroblocchi.                        |
| [**AVEncMPVQuantMatrixNonIntra**](avencmpvquantmatrixnonintra-property.md)                 | Specifica la matrice di quantizzazione Luma per macroblocchi non intra.                    |
| [**AVEncMPVScanPattern**](avencmpvscanpattern-property.md)                                 | Specifica il modello di analisi macroblocco.                                               |
| [**AVEncMPVSceneDetection**](avencmpvscenedetection-property.md)                           | Specifica il comportamento del codificatore quando rileva una nuova scena.                       |
| [**AVEncMPVUseConcealmentMotionVectors**](avencmpvuseconcealmentmotionvectors-property.md) | Specifica se il codificatore utilizza vettori di movimento di occultamento.                       |



 

### <a name="mpeg-audio-encoder-properties"></a>Proprietà del codificatore audio MPEG



| Proprietà                                                                                  | Descrizione                                                                   |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**AVEncMPACodingMode**](avencmpacodingmode-property.md)                                 | Specifica la modalità di codifica audio MPEG-1.                                     |
| [**AVEncMPACopyright**](avencmpacopyright-property.md)                                   | Specifica l'impostazione predefinita per il bit di copyright.                          |
| [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)                             | Specifica il tipo di filtro di deenfasi da usare durante la decodifica.   |
| [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md) | Specifica se aggiungere un controllo di ridondanza ciclico (CRC) all'intestazione del frame. |
| [**AVEncMPALayer**](avencmpalayer-property.md)                                           | Specifica il livello audio MPEG.                                               |
| [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)                   | Specifica l'impostazione predefinita per il bit originale.                           |
| [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)                         | Imposta il valore del bit utente privato.                                       |



 

### <a name="dolby-digital-audio-decoder-properties"></a>Proprietà del decodificatore Dolby Digital audio



| Proprietà                                                                      | Descrizione                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md) | Specifica il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli.  |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)   | Specifica l'incremento di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli. |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)             | Specifica la modalità di controllo della compressione.                                        |



 

### <a name="dolby-digital-audio-encoder-properties"></a>Proprietà del codificatore audio Dolby Digital



| Proprietà                                                                                        | Descrizione                                                                               |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AVEncDDAtoDConverterType**](avencddatodconvertertype-property.md)                           | Specifica il tipo di conversione da analogico a digitale (A/D).                                 |
| [**AVEncDDCentreDownMixLevel**](avencddcentredownmixlevel-property.md)                         | Specifica il livello downmix Center.                                                       |
| [**AVEncDDChannelBWLowPassFilter**](avencddchannelbwlowpassfilter-property.md)                 | Specifica se un filtro pass basso viene applicato ai canali di input principali.                |
| [**AVEncDDCopyright**](avencddcopyright-property.md)                                           | Specifica il flag di copyright.                                                             |
| [**AVEncDDDCHighPassFilter**](avencdddchighpassfilter-property.md)                             | Specifica se viene applicato un filtro di passaggio superiore che blocca il controller di dominio.                              |
| [**AVEncDDDialogNormalization**](avencdddialognormalization-property.md)                       | Specifica il livello di normalizzazione della finestra di dialogo.                                                 |
| [**AVEncDDDigitalDeemphasis**](avencdddigitaldeemphasis-property.md)                           | Specifica se la deenfasi digitale è.                                                    |
| [**AVEncDDDynamicRangeCompressionControl**](avencdddynamicrangecompressioncontrol-property.md) | Specifica il profilo di controllo dinamico degli intervalli.                                              |
| [**AVEncDDHeadphoneMode**](avencddheadphonemode-property.md)                                   | Specifica la modalità cuffia.                                                             |
| [**AVEncDDLFELowPassFilter**](avencddlfelowpassfilter-property.md)                             | Specifica se un filtro pass basso viene applicato al canale LFE (Low Frequency Effect). |
| [**AVEncDDLoRoCenterMixLvl \_ X10**](avencddlorocentermixlvl-x10-property.md)                    | Specifica lo spostamento del livello che viene applicato al canale centrale per lo downmixing.     |
| [**AVEncDDLoRoSurroundMixLvl \_ X10**](avencddlorosurroundmixlvl-x10-property.md)                | Specifica lo spostamento del livello che viene applicato ai canali surround per downmixing lo/ro.  |
| [**AVEncDDLtRtCenterMixLvl \_ X10**](avencddltrtcentermixlvl-x10-property.md)                    | Specifica lo spostamento del livello applicato al canale centrale per LT/RT downmixing.     |
| [**AVEncDDLtRtSurroundMixLvl \_ X10**](avencddltrtsurroundmixlvl-x10-property.md)                | Specifica lo spostamento del livello applicato ai canali surround per LT/RT downmixing.  |
| [**AVEncDDOriginalBitstream**](avencddoriginalbitstream-property.md)                           | Specifica il flag Bitstream originale.                                                    |
| [**AVEncDDPreferredStereoDownMixMode**](avencddpreferredstereodownmixmode-property.md)         | Specifica la modalità downmix stereo preferita.                                              |
| [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md)                     | Specifica il flag di informazioni di produzione audio.                                          |
| [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md)                         | Specifica il livello di combinazione.                                                               |
| [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md)                         | Specifica il tipo di chat room.                                                                  |
| [**AVEncDDRFPreEmphasisFilter**](avencddrfpreemphasisfilter-property.md)                       | Specifica l'impostazione di protezione da sovramodulazione RF.                                       |
| [**AVEncDDService**](avencddservice-property.md)                                               | Specifica il servizio audio.                                                              |
| [**AVEncDDSurround3dBAttenuation**](avencddsurround3dbattenuation-property.md)                 | Specifica se i canali surround vengono attenuati prima della codifica.                   |
| [**AVEncDDSurround90DegreeePhaseShift**](avencddsurround90degreeephaseshift-property.md)       | Specifica se un turno di fase di 90 gradi viene applicato ai canali surround.            |
| [**AVEncDDSurroundDownMixLevel**](avencddsurrounddownmixlevel-property.md)                     | Specifica il livello di combinazione del contorno.                                                    |
| [**AVEncDDSurroundExMode**](avencddsurroundexmode-property.md)                                 | Specifica se il flusso audio è codificato in surround es.                             |



 

### <a name="digital-signal-processing-dsp-properties"></a>Proprietà di elaborazione dei segnali digitali (DSP)



| Proprietà                                                                | Descrizione                               |
|-------------------------------------------------------------------------|-------------------------------------------|
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md) | Abilita o Disabilita l'uguaglianza di sonorità |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                   | Abilita o Disabilita il riempimento degli speaker          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'API codec](codec-api-reference.md)
</dt> </dl>

 

 



