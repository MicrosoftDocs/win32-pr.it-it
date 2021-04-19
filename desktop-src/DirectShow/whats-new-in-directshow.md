---
description: Novità di DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Novità di DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319536"
---
# <a name="whats-new-in-directshow"></a>Novità di DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Novità di DirectShow in Windows 7

Nuove interfacce:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtri nuovi o aggiornati:

-   [**Decoder audio Microsoft MPEG-1/gg/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Decoder video Microsoft MPEG-2**](microsoft-mpeg-2-video-decoder.md)

Gli algoritmi "connessione intelligente" sono stati modificati per supportare i filtri preferiti e bloccati. Per informazioni dettagliate, vedere [connessione intelligente](intelligent-connect.md).

Riproduzione DVD: nuove opzioni per il metodo [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

## <a name="whats-new-for-directshow-in-windows-vista"></a>Novità di DirectShow in Windows Vista

-   DirectShow fa ora parte del Windows SDK. Le intestazioni, le librerie, gli esempi e gli strumenti di DirectShow non sono più inclusi in DirectX SDK.
-   DirectX Video Acceleration (DXVA) 2,0 contiene molti miglioramenti di DXVA 1,0.

    -   La pipeline video hardware è stata notevolmente migliorata.
    -   I componenti quali i decodificatori possono accedere direttamente a DXVA 2,0 senza comunicarlo tramite il renderer video.
    -   Il Gestione dispositivi Direct3D consente ai componenti di condividere lo stesso dispositivo Direct3D.

    Per ulteriori informazioni su DXVA 2,0, vedere la documentazione di [DirectX Video Acceleration 2,0](../medfound/directx-video-acceleration-2-0.md) , che fa parte della documentazione [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .

-   Il [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR) è un potente nuovo renderer video, che condivide lo stesso modello di plug-in della versione Media Foundation di EVR. Per ulteriori informazioni su EVR, vedere la documentazione [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .
-   Supporto per l'acquisizione di Windows Vista Display Driver Model (WDDM). Questa funzionalità consente ai filtri di sfruttare appieno le schede video con acquisizione video integrata, per ridurre le copie non necessarie tra memoria video e memoria di sistema. Per altre informazioni, vedere [uso di WDDM Capture in DirectShow](using-wddm-capture-in-directshow.md).
-   Il decoder audio MPEG-1 Layer II ora usa l'aritmetica a virgola mobile per migliorare la qualità della decodifica.
-   Miglioramenti della riproduzione DVD. Per informazioni dettagliate, vedere [miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Migliore supporto in modalità Trick: transizioni uniformi tra le tariffe; transizioni tra la riproduzione in diretta e viceversa; supporto per la riproduzione audio durante l'avanzamento rapido e viceversa.
    -   Caching migliorato. Le applicazioni possono impostare la quantità di dati che il navigatore DVD legge in anticipo. L'impostazione di una cache più ampia può estendere la durata della batteria e abilitare la riproduzione invisibile all'utente (dopo che l'unità si è interrotta). Per altre informazioni, vedere [**\_ \_ flag di opzione DVD**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Dispositivi audio endpoint: le applicazioni possono associare il [filtro renderer DirectSound](directsound-renderer-filter.md) a un particolare dispositivo di endpoint audio. Le applicazioni possono usare l'API del dispositivo multimediale (MMDevice) per enumerare e selezionare il dispositivo endpoint. Per ulteriori informazioni, vedere la documentazione principale dell'API audio nell'Windows SDK.
-   I filtri seguenti sono stati rimossi da Windows Vista:
    -   [Filtro sink IP BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtro deframer SLIP BDA](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtro decodificatore CC](cc-decoder-filter.md)
    -   [Filtro codec VBI NABTS/FEC](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtro del decompressore QT](qt-decompressor-filter.md)
    -   [Filtro del parser film QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtro codec WST](wst-codec-filter.md)
    -   [Filtro decodificatore WST](wst-decoder-filter.md)
-   Il codice di proxy/stub per molte interfacce DirectShow è stato spostato da quartz.dll a proppage.dll. Questo codice è stato rimosso dal quartz.dll perché non era destinato all'uso da applicazioni. Tuttavia, è utile per il debug, perché consente a un'applicazione di test di connettersi in modalità remota a un grafico di filtro DirectShow in un altro processo. Per utilizzare questa funzionalità in Windows Vista, è necessario prima registrare proppage.dll. Questa DLL è disponibile nella directory Windows SDK Tools. Per ulteriori informazioni, vedere [caricamento di un grafico da un processo esterno](loading-a-graph-from-an-external-process.md).

 

 
