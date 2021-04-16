---
title: Piattaforma multimediale
description: Media Foundation e DirectShow forniscono la base per il supporto multimediale in Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517056"
---
# <a name="media-platform"></a>Piattaforma multimediale

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) e [DirectShow](/windows/desktop/DirectShow/directshow) forniscono la base per il supporto multimediale in Windows. Media Foundation è stato introdotto in Windows Vista come sostituzione di DirectShow. In Windows 7, Media Foundation è stato migliorato per offrire un supporto migliore per il formato, incluso *MPEG-4*, nonché il supporto per i dispositivi di acquisizione video e i codec hardware.

## <a name="format-support"></a>Supporto del formato

In Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) offre un supporto completo per i formati che include codec per video *H. 264* , *MJPEG* e *MP3*; nuove origini per *MP4*, *3GP*, *AAC* audio e *AVI*; e i nuovi sink di file per *MP4*, *3GP* e *MP3*. (Vedere [formati multimediali supportati in Media Foundation](../medfound/supported-media-formats-in-media-foundation.md)).

## <a name="hardware-devices"></a>Dispositivi hardware

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) supporta ora i seguenti tipi di dispositivi hardware nella pipeline audio/video:

-   Dispositivi di acquisizione video *UVC 1,1* , ad esempio webcam
-   Dispositivi di acquisizione audio
-   Codificatori e decodificatori hardware
-   Processori video hardware, ad esempio convertitori di spazio colore

I codec hardware possono eseguire una transcodifica video molto rapida. Si supponga, ad esempio, di voler trasferire un file di *Windows Media video (WMV)* a un telefono cellulare che supporta solo file *3GP* . Con un codificatore hardware, il file può essere transcodificato "in base alle esigenze" immediatamente prima del trasferimento al dispositivo.

I dispositivi hardware sono rappresentati in [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) da un oggetto proxy e vengono usati nella pipeline esattamente come i componenti basati su software. Vedere Novità [per Media Foundation](../medfound/whats-new-for-media-foundation.md).

## <a name="simplified-programming-model"></a>Modello di programmazione semplificato

In Windows Vista [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) esposto un set di API relativamente di basso livello. Queste API sono flessibili, ma potrebbero non essere appropriate per l'esecuzione di attività. Windows 7 aggiunge nuove API di alto livello che semplificano la scrittura di applicazioni multimediali in *C++*. Queste nuove API di alto livello includono:

-   **MFPlay**. Queste API sono progettate per la riproduzione audio e video. Supportano le operazioni di riproduzione tipiche (arresto, pausa, riproduzione, ricerca, controllo della frequenza, volume audio e così via), nascondendo al tempo stesso i dettagli delle API di basso livello (la sessione e i livelli della topologia).
-   **Lettore di origine**. È possibile usare queste API per eseguire il pull di dati non elaborati o decodificati da un file multimediale, senza conoscere il formato sottostante. Ad esempio, è possibile ottenere una bitmap di anteprima da un file video o ottenere frame video dinamici da una webcam.
-   **Sink writer**. È possibile usare queste API per creare file multimediali passando dati non compressi o codificati. Ad esempio, è possibile ricodificare o remixare un file video.
-   **Transcodifica**. Queste API sono destinate agli scenari più comuni di codifica audio e video.

## <a name="platform-improvements"></a>Miglioramenti della piattaforma

Windows 7 include numerosi miglioramenti alle API della piattaforma [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) sottostante. Le applicazioni avanzate possono usare direttamente queste API; altre applicazioni otterranno i vantaggi indirettamente. Questi vantaggi includono:

-   Miglioramenti apportati alla pipeline video per ridurre il consumo di energia e l'utilizzo della memoria del video.
-   Nuove API di elaborazione video *DVXA* , che usano un modello di composizione più flessibile e sono più adatte per i formati video *HD* .
-   Miglioramenti alla modalità di enumerazione e gestione dei plug-in (origini e decodificatori).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 