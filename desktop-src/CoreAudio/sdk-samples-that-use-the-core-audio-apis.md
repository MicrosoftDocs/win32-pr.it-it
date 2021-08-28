---
description: Esempi di SDK che usano le API audio di base
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Esempi di SDK che usano le API audio di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f875095579b40c6646d89e31328c148c5724c309
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479697"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Esempi di SDK che usano le API audio di base

L Windows SDK include gli esempi di codice seguenti che illustrano l'uso delle API audio di base. Gli esempi seguenti si trovano nella directory %MSSdk% samples multimedia audio, dove \\ \\ %MSSdk% è la directory radice dell'installazione di Windows SDK nel \\ computer.




| Esempio | Deascription | 
|--------|--------------|
| <a href="aecmicarray.md">AECMicArray</a> | Questo esempio usa le API MMDevice, WASAPI, DeviceTopology ed EndpointVolume per acquisire un flusso vocale di alta qualità. L'esempio supporta l'annullamento dell'eco acustica (AEC) e l'elaborazione di matrici di microfoni usando il DMO AEC chiamato anche DSP di acquisizione vocale fornito da Microsoft. | 
| <a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a> | Questa applicazione di esempio usa le API core audio per acquisire dati audio da un dispositivo di input, specificato dall'utente e scrive i dati in un oggetto denominato in modo univoco. File WAV nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata su eventi. | 
| <a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a> | Questa applicazione di esempio usa le API core audio per acquisire dati audio da un dispositivo di input, specificato dall'utente e scrive i dati in un oggetto denominato in modo univoco. File WAV nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata su timer. | 
| <a href="duckingcapturesample.md">EsempiocaptureSample</a> | Questa applicazione di esempio illustra l'apertura e la chiusura dei flussi di comunicazione e la causa degli eventi di disaccodamento che un'applicazione può ottenere per implementare l'attenuazione del flusso. Questa applicazione implementa un client di chat che usa le API Core Audio per leggere i dati audio da un dispositivo di comunicazione e riprodurlo nel dispositivo di output. | 
| <a href="endpointvolume.md">EndpointVolume</a> | Questa applicazione di esempio usa le API core audio per modificare il volume del dispositivo, specificato dall'utente. | 
| <a href="osd.md">OSD</a> | Questo esempio usa le API MMDevice ed EndpointVolume per implementare una visualizzazione su schermo che mostra le modifiche del volume al flusso di output riprodotto tramite il dispositivo endpoint di rendering audio predefinito. La visualizzazione su schermo viene visualizzata quando l'utente regola il livello del volume nel programma di controllo del volume Windows, Sndvol.exe, e scompare dopo che il livello del volume rimane invariato per un breve periodo di tempo. | 
| <a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a> | Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. In questo esempio viene illustrata la memorizzazione nel buffer basata su eventi per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio. | 
| <a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a> | Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. In questo esempio viene illustrata la memorizzazione nel buffer basata su timer per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio. | 
| <a href="rendersharedeventdriven.md">RenderSharedEventDriven</a> | Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. In questo esempio viene illustrata la memorizzazione nel buffer basata su eventi per un client di rendering in modalità condivisa. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio. | 
| <a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a> | Questa applicazione di esempio usa le API Core Audio per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. In questo esempio viene illustrata la memorizzazione nel buffer basata su timer per un client di rendering in modalità condivisa. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio. | 
| WinAudio | Questo esempio usa l'API MMDevice e WASAPI per riprodurre e acquisire flussi audio. L'interfaccia utente di questa applicazione di esempio consente agli utenti di selezionare i dispositivi endpoint audio, di modificare il livello di volume della sessione audio locale e di riprodurre i file wav e l'input del microfono.<blockquote>[!Note]<br />Questo esempio è stato deprecato in Windows 7.</blockquote><br /> | 




 

È possibile scaricare l'SDK Windows dal sito [Web dell'Area download microsoft Windows SDK.](https://developer.microsoft.com/windows/downloads/sdk-archive/)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle WINDOWS Core Audio](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




