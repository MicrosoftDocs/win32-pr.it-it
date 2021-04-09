---
description: Enumerazioni API codec
ms.assetid: 5d6e48cb-d181-448e-a96e-e5ab500427d7
title: Enumerazioni API codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c97da1fe45aba1d81e7036fa7ba6e75fc225a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965669"
---
# <a name="codec-api-enumerations"></a>Enumerazioni API codec



| Enumerazione                                                                              | Descrizione                                                                                               |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)                                   | Specifica la configurazione dell'altoparlante per i canali audio nel flusso di bit audio.                       |
| [**eAVDDSurroundMode**](/windows/desktop/api/codecapi/ne-codecapi-eavddsurroundmode)                                           | Specifica se l'audio è codificato in Dolby surround.                                                 |
| [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)                                     | Specifica se un decodificatore AAC USA equazioni downmix standard MPEG-2/MPEG-4 stereo.                    |
| [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)                                       | Specifica se il flusso audio di input è stereo o doppio mono.                                          |
| [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)                     | Specifica il modo in cui il decodificatore riproduce audio mono doppio.                                                     |
| [**eAVDecDDOperationalMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecddoperationalmode)                               | Specifica la modalità di controllo della compressione per un flusso audio Dolby AC-3.                                     |
| [**eAVDecHEAACDynamicRangeControl**](/windows/desktop/api/codecapi/ne-codecapi-eavdecheaacdynamicrangecontrol)                 | Specifica se un decodificatore AAC esegue il controllo dinamico degli intervalli.                                          |
| [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype)                             | Specifica il modo in cui il flusso video decodificato è interlacciato.                                                     |
| [**eAVDecVideoSoftwareDeinterlaceMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideosoftwaredeinterlacemode)         | Specifica la modalità di deinterlacciamento del software di un decodificatore video.                                                    |
| [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel)                               | Specifica il livello di risparmio energia di un decodificatore video.                                                      |
| [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)                         | Specifica se è abilitata l'uguaglianza di sonorità in un decoder audio o in un processore di segnale digitale (DSP). |
| [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)                                           | Specifica se il riempimento degli altoparlanti è abilitato in un decodificatore audio o in un DSP.                                     |
| [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)                                       | Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.                                      |
| [**Enumerazione eAVEncAudioInputContent**](/windows/win32/api/codecapi/ne-codecapi-eavencaudioinputcontent)                   | Specifica se il contenuto audio contiene musica o voce.                                              |
| [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)                       | Specifica la modalità di controllo della frequenza.                                                                          |
| [**eAVEncCommonStreamEndHandling**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonstreamendhandling)                   | Specifica se il codificatore ignora gruppi parziali di immagini (GOPs) alla fine del flusso.        |
| [**eAVEncDDAtoDConverterType**](/windows/win32/api/codecapi/ne-codecapi-eavencddatodconvertertype)                           | Specifica il tipo di conversione da analogico a digitale (A/D) per un flusso audio Dolby Digital.                |
| [**eAVEncDDDynamicRangeCompressionControl**](/windows/win32/api/codecapi/ne-codecapi-eavencdddynamicrangecompressioncontrol) | Specifica il profilo di controllo dinamico degli intervalli in un flusso audio Dolby Digital.                              |
| [**eAVEncDDHeadphoneMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddheadphonemode)                                   | Specifica la modalità cuffia per un flusso audio Dolby Digital.                                                |
| [**eAVEncDDPreferredStereoDownMixMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddpreferredstereodownmixmode)         | Specifica la modalità downmix stereo preferita per un flusso audio Dolby Digital.                             |
| [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)                         | Specifica il tipo di stanza per un flusso audio Dolby Digital.                                                 |
| [**eAVEncDDService**](/windows/desktop/api/codecapi/ne-codecapi-eavencddservice)                                               | Specifica il servizio audio contenuto in un flusso audio Dolby Digital.                                    |
| [**eAVEncDDSurroundExMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencddsurroundexmode)                                 | Specifica se un flusso audio Dolby Digital è codificato in Dolby Digital Surround es.                   |
| [**eAVEncInputVideoSystem**](/windows/desktop/api/codecapi/ne-codecapi-eavencinputvideosystem)                                 | Specifica l'intervallo nominale per un'origine video.                                                           |
| [**eAVEncMPACodingMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpacodingmode)                                       | Specifica la modalità di codifica audio MPEG.                                                                   |
| [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype)                                   | Specifica il tipo di filtro di deenfasi da usare durante la decodifica.                               |
| [**eAVEncMPALayer**](/windows/win32/api/codecapi/ne-codecapi-eavencmpalayer)                                                 | Specifica il livello audio MPEG.                                                                           |
| [**eAVEncMPVFrameFieldMode**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvframefieldmode)                               | Specifica se il codificatore produce campi codificati o frame codificati.                                  |
| [**eAVEncMPVIntraVLCTable**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvintravlctable)                                 | Specifica la tabella di codifica a lunghezza variabile (VLC) da usare per la codifica dell'entropia.                             |
| [**eAVEncMPVLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvlevel)                                                 | Specifica il profilo MPEG-2.                                                                             |
| [**eAVEncMPVProfile**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvprofile)                                             | Specifica il profilo MPEG-2.                                                                             |
| [**eAVEncMPVQScaleType**](/windows/desktop/api/codecapi/ne-codecapi-eavencmpvqscaletype)                                       | Specifica se la scala del quantizzatore è lineare o non lineare.                                            |
| [**eAVEncMPVScanPattern**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscanpattern)                                     | Specifica il modello di analisi macroblocco.                                                                    |
| [**eAVEncMPVSceneDetection**](/windows/win32/api/codecapi/ne-codecapi-eavencmpvscenedetection)                               | Specifica il comportamento del codificatore quando rileva una nuova scena.                                            |
| [**eAVEncMuxOutput**](/windows/win32/api/codecapi/ne-codecapi-eavencmuxoutput)                                               | Specifica il tipo di flusso di output prodotto da un multiplexer.                                            |
| [**eAVEncVideoChromaResolution**](/windows/win32/api/codecapi/ne-codecapi-eavencvideochromaresolution)                       | Specifica la risoluzione Chroma.                                                                              |
| [**eAVEncVideoChromaSubsampling**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideochromasubsampling)                     | Specifica la posizione Chroma.                                                                                  |
| [**eAVEncVideoColorLighting**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorlighting)                             | Specifica le condizioni di illuminazione desiderate per la visualizzazione di un'origine video.                                    |
| [**eAVEncVideoColorNominalRange**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolornominalrange)                     | Specifica l'intervallo nominale per un'origine video.                                                           |
| [**eAVEncVideoColorPrimaries**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolorprimaries)                           | Specifica le tonalità primarie del video.                                                               |
| [**eAVEncVideoColorTransferFunction**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransferfunction)             | Specifica la funzione di conversione da SOTTOCAMPIONATURA a RGB.                                                     |
| [**eAVEncVideoColorTransferMatrix**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideocolortransfermatrix)                 | Specifica la matrice di conversione dallo spazio colore Cb'Cr "allo spazio colore SOTTOCAMPIONATURA".                  |
| [**eAVEncVideoFilmContent**](/windows/win32/api/codecapi/ne-codecapi-eavencvideofilmcontent)                                 | Specifica se l'origine originale del video di input è film o video.                               |
| [**eAVEncVideoOutputFrameRateConversion**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputframerateconversion)     | Specifica se il codificatore converte la frequenza dei fotogrammi.                                                    |
| [**eAVEncVideoOutputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavencvideooutputscantype)                           | Specifica il modo in cui il codificatore interlaccierà il video di output.                                                    |
| [**eAVEncVideoSourceScanType**](/windows/desktop/api/codecapi/ne-codecapi-eavencvideosourcescantype)                           | Specifica se i fotogrammi di input per un codificatore sono progressivi o interlacciati.                          |
| [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode)                                           | Specifica la velocità di decodifica dei video.                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'API codec](codec-api-reference.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 
