---
title: Piattaforma multimediale
description: Media Foundation e DirectShow la base per il supporto multimediale in Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a4db7d84745f64f3fe80faed267e58d1f5ddbce4ab82ed75b38453f82b0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964580"
---
# <a name="media-platform"></a>Piattaforma multimediale

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) e [DirectShow](/windows/desktop/DirectShow/directshow) la base per il supporto multimediale in Windows. Media Foundation è stato introdotto in Windows Vista come sostituzione per DirectShow. In Windows 7, Media Foundation è stato migliorato per offrire un supporto migliore per il formato, tra cui *MPEG-4,* nonché per i dispositivi di acquisizione video e i codec hardware.

## <a name="format-support"></a>Supporto del formato

In Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) supporto completo del formato che include codec per video *H.264,* *MJPEG* e *MP3;* nuove origini per *MP4,* *3GP,* audio *AAC* e *AVI;* e nuovi sink di file per *MP4,* *3GP* e *MP3.* Vedere [Formati multimediali supportati in Media Foundation](../medfound/supported-media-formats-in-media-foundation.md).

## <a name="hardware-devices"></a>Dispositivi hardware

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) supporta ora i tipi di dispositivi hardware seguenti nella pipeline audio/video:

-   Dispositivi di acquisizione video *UVC 1.1,* ad esempio webcam
-   Dispositivi di acquisizione audio
-   Codificatori e decodificatori hardware
-   Processori video hardware, ad esempio convertitori di spazi colori

I codec hardware possono eseguire una transcoddtura video molto veloce. Si supponga, ad esempio, di voler trasferire un file *Windows Media Video (WMV)* in un telefono cellulare che supporta solo *file 3GP.* Con un codificatore hardware, il file può essere transcodificato "in base alle esigenze" immediatamente prima di trasferirlo al dispositivo.

I dispositivi hardware sono rappresentati in [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) da un oggetto proxy e vengono usati nella pipeline esattamente come i componenti basati su software. Vedere [Novità di Media Foundation](../medfound/whats-new-for-media-foundation.md).

## <a name="simplified-programming-model"></a>Modello di programmazione semplificato

In Windows [Vista, Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) ha esposto un set di API di livello relativamente basso. Queste API sono flessibili, ma potrebbero non essere appropriate per l'esecuzione di attività. Windows 7 aggiunge nuove API di alto livello che semplificano la scrittura di applicazioni multimediali in *C++.* Queste nuove API di alto livello includono:

-   **MFPlay**. Queste API sono progettate per la riproduzione audio e video. Supportano le normali operazioni di riproduzione (arresto, sospensione, riproduzione, ricerca, controllo della frequenza, volume audio e così via), nascondendo al tempo stesso i dettagli delle API di basso livello (i livelli di sessione e topologia).
-   **Lettore di origine.** È possibile usare queste API per eseguire il pull di dati non elaborati o decodificati da un file multimediale, senza conoscere il formato sottostante. Ad esempio, è possibile ottenere una bitmap di anteprima da un file video o ottenere fotogrammi video live da una webcam.
-   **Writer di sink**. È possibile usare queste API per creare file multimediali passando dati non compressi o codificati. Ad esempio, è possibile codificare nuovamente o remixare un file video.
-   **Transcodifica**. Queste API hanno come destinazione gli scenari di codifica audio e video più comuni.

## <a name="platform-improvements"></a>Miglioramenti della piattaforma

Windows 7 include numerosi miglioramenti alle API [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) della piattaforma sottostante. Le applicazioni avanzate possono usare direttamente queste API. altre applicazioni otterrà i vantaggi indirettamente. Questi vantaggi includono:

-   Miglioramenti della pipeline video per ridurre il consumo di energia e l'utilizzo della memoria video.
-   Nuove API di elaborazione video *DVXA,* che usano un modello di composizione più flessibile e sono più adatte per i formati video *HD.*
-   Miglioramenti al modo in cui i plug-in (origini e decodificatori) vengono enumerati e gestiti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 