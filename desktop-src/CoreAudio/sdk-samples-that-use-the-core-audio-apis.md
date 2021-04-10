---
description: Esempi di SDK che usano le API audio principali
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Esempi di SDK che usano le API audio principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966178"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Esempi di SDK che usano le API audio principali

Il Windows SDK include gli esempi di codice seguenti che illustrano l'uso delle API audio di base. Gli esempi seguenti si trovano nella directory% MSSdk% \\ Samples \\ Multimedia \\ audio, dove% MSSdk% è la directory radice dell'installazione del Windows SDK nel computer.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Esempio</th>
<th>Deascription</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aecmicarray.md">AECMicArray</a></td>
<td>Questo esempio usa le API MMDevice, WASAPI, DeviceTopology e EndpointVolume per acquisire un flusso vocale di alta qualità. L'esempio TImpossibile supporta l'elaborazione Echo Echo Cancel (AEC) e la matrice di microfoni usando l'AEC DMO chiamato anche il DSP di acquisizione vocale fornito da Microsoft.</td>
</tr>
<tr class="even">
<td><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></td>
<td>Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input, specificato dall'utente e lo scrive in un nome univoco. File WAV nella directory corrente. In questo esempio viene illustrata la memorizzazione nel buffer basata sugli eventi.</td>
</tr>
<tr class="odd">
<td><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></td>
<td>Questa applicazione di esempio usa le API audio principali per acquisire i dati audio da un dispositivo di input, specificato dall'utente e lo scrive in un nome univoco. File WAV nella directory corrente. Questo esempio illustra il buffering basato sul timer.</td>
</tr>
<tr class="even">
<td><a href="duckingcapturesample.md">DuckingCaptureSample</a></td>
<td>Questa applicazione di esempio illustra l'apertura e la chiusura di flussi di comunicazione e la generazione di eventi ducking che un'applicazione può ottenere per implementare l'attenuazione del flusso. Questa applicazione implementa un client di chat che usa le API audio principali per leggere i dati audio da un dispositivo di comunicazione e riprodurli sul dispositivo di output.</td>
</tr>
<tr class="odd">
<td><a href="endpointvolume.md">EndpointVolume</a></td>
<td>Questa applicazione di esempio usa le API audio principali per modificare il volume del dispositivo, specificato dall'utente.</td>
</tr>
<tr class="even">
<td><a href="osd.md">OSD</a></td>
<td>Questo esempio usa le API MMDevice e EndpointVolume per implementare una visualizzazione sullo schermo che mostra le modifiche del volume al flusso di output che riproduce il dispositivo dell'endpoint di rendering audio predefinito. La visualizzazione sullo schermo viene visualizzata quando l'utente regola il livello del volume nel programma di controllo del volume di Windows, Sndvol.exe e scompare dopo che il livello del volume rimane invariato per un breve periodo di tempo.</td>
</tr>
<tr class="odd">
<td><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></td>
<td>Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. In questo esempio viene illustrato il buffer basato sugli eventi per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</td>
</tr>
<tr class="even">
<td><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></td>
<td>Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità esclusiva. Per un flusso in modalità esclusiva, il client condivide il buffer dell'endpoint con il dispositivo audio.</td>
</tr>
<tr class="odd">
<td><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></td>
<td>Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. Questo esempio illustra il buffering basato sugli eventi per un client di rendering in modalità condivisa. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</td>
</tr>
<tr class="even">
<td><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></td>
<td>Questa applicazione di esempio usa le API audio principali per eseguire il rendering dei dati audio in un dispositivo di output, specificato dall'utente. Questo esempio illustra il buffering basato sul timer per un client di rendering in modalità condivisa. Per un flusso in modalità condivisa, il client condivide il buffer dell'endpoint con il motore audio.</td>
</tr>
<tr class="odd">
<td>WinAudio</td>
<td>Questo esempio usa l'API MMDevice e WASAPI per riprodurre e acquisire flussi audio. L'interfaccia utente di questa applicazione di esempio consente agli utenti di selezionare dispositivi endpoint audio, modificare il livello del volume della sessione audio locale e riprodurre i file WAV e l'input del microfono.
<blockquote>
[!Note]<br />
Questo esempio è stato deprecato in Windows 7.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

È possibile scaricare il Windows SDK dal sito Web dell' [area download Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




