---
title: Informazioni di riferimento su AVIFile
description: Informazioni di riferimento su AVIFile
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b4bbda5374f5b1418c166aae5efcc06168b522b2cae0f3b6d2c8fe3c069c36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808321"
---
# <a name="avifile-reference"></a>Informazioni di riferimento su AVIFile

Questa sezione descrive le funzioni, le strutture e le macro per le applicazioni che usano i servizi AVIFile. Questi elementi sono raggruppati nel modo seguente:

## <a name="avifile-library-operations"></a>Operazioni della libreria AVIFile

-   [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a>Apertura e chiusura di file AVI

-   [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a>Lettura da un file

-   [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a>Scrittura in un file

-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a>Uso degli Appunti

-   [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a>Apertura e chiusura Flussi

-   [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a>Lettura delle informazioni sul flusso

-   [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a>Decompressione dei dati video in un flusso

-   [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a>Creazione di un file da Flussi

-   [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a>Scrittura di singoli Flussi

-   [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a>Ricerca della posizione iniziale in un flusso

-   [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a>Ricerca di fotogrammi chiave e di esempio

-   [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a>Passaggio tra esempi e ora

-   [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a>Creazione di Flussi

-   [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a>Modifica di AVI Flussi

-   [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni e macro AVIFile](avifile-functions-and-macros.md)
</dt> </dl>

 

 




