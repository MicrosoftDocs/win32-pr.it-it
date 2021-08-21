---
description: Enumerazioni api codec
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Enumerazioni api codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28b82d73d6bd6fefed5f3c9296a666d1053cd71b074a782858b31e94dc3a3ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079331"
---
# <a name="codec-api-enumerations"></a>Enumerazioni api codec



| Enumerazione                                                                              | Descrizione                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Specifica la configurazione del parlante per i canali audio nel flusso di bit audio.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Specifica se l'audio è codificato in Dolby Surround.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Specifica se un decodificatore AAC usa equazioni downmix stereo MPEG-2/MPEG-4 standard.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Specifica se il flusso audio di input è stereo o doppio mono.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Specifica la modalità di riproduzione dell'audio doppio mono da parte del decodificatore.                                                     |
| [**eAVDecddOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Specifica la modalità di controllo della compressione per un flusso audio Dolby AC-3.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Specifica se un decodificatore AAC esegue il controllo dinamico dell'intervallo.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Specifica la modalità di interlacciazione del flusso video decodificato.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Specifica la modalità deinterlace software di un decodificatore video.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Specifica il livello di risparmio energia di un decodificatore video.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Specifica se l'equalizzazione del volume è abilitata in un decodificatore audio o in un processore di segnale digitale (DSP). |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Specifica se il riempimento del parlante è abilitato in un decodificatore audio o in un DSP.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.                                      |
| [**Enumerazione eAVEncAudioInputContent**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Specifica se il contenuto audio contiene musica o voce.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Specifica la modalità di controllo della frequenza.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Specifica se il codificatore rimuove gruppi parziali di immagini (GOP) alla fine del flusso.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Specifica il tipo di conversione da analogico a digitale (A/D) per un flusso audio Dolby Digital.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Specifica il profilo di controllo dell'intervallo dinamico in un flusso audio Dolby Digital.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Specifica la modalità cuffia per un flusso audio Dolby Digital.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Specifica la modalità downmix stereo preferita per un flusso audio Dolby Digital.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Specifica il tipo di stanza per un flusso audio Dolby Digital.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Specifica il servizio audio contenuto in un flusso audio Dolby Digital.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Specifica se un flusso audio Dolby Digital è codificato in Dolby Digital Surround EX.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Specifica l'intervallo nominale per un'origine video.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Specifica la modalità di codifica audio MPEG.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Specifica il tipo di filtro di de-enfasi che deve essere usato durante la decodifica.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Specifica il livello audio MPEG.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Specifica se il codificatore produce campi codificati o fotogrammi codificati.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Specifica quale tabella di codifica a lunghezza variabile (VLC) usare per la codifica entropia.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Specifica il profilo MPEG-2.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Specifica il profilo MPEG-2.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Specifica se la scala quantizzante è lineare o non lineare.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Specifica il modello di analisi macroblock.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Specifica il comportamento del codificatore quando rileva una nuova scena.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Specifica il tipo di flusso di output prodotto da un multiplexer.                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Specifica la risoluzione della croma.                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Specifica il siting di chroma.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Specifica le condizioni di illuminazione per la visualizzazione di un'origine video.                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Specifica l'intervallo nominale per un'origine video.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Specifica i colori primari del video.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Specifica la funzione di conversione da R'G'B' a RGB.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Specifica la matrice di conversione dallo spazio colori Y'Cb'Cr' allo spazio colori R'G'B'.                  |
| [**eAVEncVideoContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Specifica se l'origine originale del video di input è film o video.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Specifica se il codificatore converte la frequenza dei fotogrammi.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Specifica il modo in cui il codificatore interlaccia il video di output.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Specifica se i fotogrammi di input per un codificatore sono progressivi o interlacciati.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Specifica la velocità di decodifica video.                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API codec](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
