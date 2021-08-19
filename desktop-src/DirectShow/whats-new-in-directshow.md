---
description: Novità di DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Novità di DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd05d11931d7c23a078643724b99dfed84b65e3a7db3e4ed60df9cd2a3273f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071885"
---
# <a name="whats-new-in-directshow"></a>Novità di DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Novità di DirectShow in Windows 7

Nuove interfacce:

-   [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Filtri nuovi o aggiornati:

-   [**Decodificatore audio MPEG-1/DD/AAC Microsoft**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Decodificatore video MPEG-2 Microsoft**](microsoft-mpeg-2-video-decoder.md)

Gli algoritmi di "connessione intelligente" sono stati modificati per supportare i filtri preferiti e bloccati. Per informazioni dettagliate, vedere [Intelligent Connessione](intelligent-connect.md).

Riproduzione DVD: nuove opzioni per il [**metodo IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

## <a name="whats-new-for-directshow-in-windows-vista"></a>Novità di DirectShow in Windows Vista

-   DirectShow fa ora parte di Windows SDK. Le DirectShow, le librerie, gli esempi e gli strumenti non sono più inclusi in DirectX SDK.
-   DirectX Video Acceleration (DXVA) 2.0 contiene molti miglioramenti di DXVA 1.0.

    -   La pipeline video hardware è stata migliorata in modo significativo.
    -   Componenti come i decodificatori possono accedere direttamente a DXVA 2.0 senza comunicare tramite il renderer video.
    -   Gestione dispositivi Direct3D consente ai componenti di condividere lo stesso dispositivo Direct3D.

    Per altre informazioni su DXVA 2.0, vedere la documentazione di [DirectX Video Acceleration 2.0,](../medfound/directx-video-acceleration-2-0.md) che fa parte della documentazione [Microsoft Media Foundation.](../medfound/microsoft-media-foundation-sdk.md)

-   [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) è un potente nuovo renderer video, che condivide lo stesso modello di plug-in della versione Media Foundation del sistema EVR. Per altre informazioni sull'EVR, vedere la [documentazione Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) EVR.
-   Supporto per Windows'acquisizione WDDM (Vista Display Driver Model). Questa funzionalità consente ai filtri di sfruttare al meglio le schede video con l'acquisizione video integrata, per ridurre le copie non necessarie tra la memoria video e la memoria di sistema. Per altre informazioni, vedere [Uso dell'acquisizione WDDM in DirectShow](using-wddm-capture-in-directshow.md).
-   Il decodificatore audio MPEG-1 Layer II usa ora l'aritmetica a virgola mobile, per una migliore qualità di decodifica.
-   Miglioramenti della riproduzione di DVD. Per informazioni dettagliate, vedere [Miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Supporto migliore della modalità trick: transizioni uniformi tra le tariffe; transizioni tra riproduzione in avanti e inversa; supporto per la riproduzione audio durante l'avanzamento rapido e la retromarcia.
    -   Memorizzazione nella cache avanzata. Le applicazioni possono impostare la quantità di dati letti in anticipo da DVD Navigator. L'impostazione di una cache più grande può estendere la durata della batteria e abilitare la riproduzione invisibile all'utente (dopo la rotazione dell'unità). Per altre informazioni, vedere [**DVD \_ OPTION \_ FLAG**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Dispositivi end-point audio: le applicazioni possono associare [il filtro renderer DirectSound](directsound-renderer-filter.md) a un dispositivo finale audio specifico. Le applicazioni possono usare l'API MmDevice (Multimedia Device) per enumerare e selezionare il dispositivo dell'end-point. Per altre informazioni, vedere la documentazione dell'API Audio Core in Windows SDK.
-   I filtri seguenti sono stati rimossi da Windows Vista:
    -   [Filtro sink IP BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Filtro del deframer SLIP BDA](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Filtro decodificatore CC](cc-decoder-filter.md)
    -   [Filtro codec VBI NABTS/FEC](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Filtro decompressore QT](qt-decompressor-filter.md)
    -   [Filtro del parser di film QuickTime](quicktime-movie-parser-filter.md)
    -   [Filtro codec WST](wst-codec-filter.md)
    -   [Filtro decodificatore WST](wst-decoder-filter.md)
-   Il codice proxy/stub per molte delle interfacce DirectShow è stato spostato da quartz.dll a proppage.dll. Questo codice è stato rimosso quartz.dll perché non era destinato all'uso da parte delle applicazioni. Tuttavia, è utile per il debug, perché consente a un'applicazione di test di connettersi in remoto a un grafico DirectShow filtro in un altro processo. Per usare questa funzionalità in Windows Vista, è necessario prima registrare proppage.dll. Questa DLL è disponibile nella directory degli strumenti Windows SDK. Per altre informazioni, vedere [Caricamento di un Graph da un processo esterno.](loading-a-graph-from-an-external-process.md)

 

 
