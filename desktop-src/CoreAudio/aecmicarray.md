---
description: Questo esempio usa le API audio principali per acquisire un flusso vocale di alta qualità. L'esempio supporta l'elaborazione dell'annullamento acustico Echo (AEC) e dell'array di microfoni usando l'AEC DMO, detto anche DSP di acquisizione vocale, fornito da Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127678"
---
# <a name="aecmicarray"></a>AECMicArray

Questo esempio usa le API audio principali per acquisire un flusso vocale di alta qualità. L'esempio supporta l'elaborazione dell'annullamento acustico Echo (AEC) e dell'array di microfoni usando l'AEC DMO, detto anche DSP di acquisizione vocale, fornito da Microsoft.

Questo argomento contiene le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   [MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.
-   [WASAPI](wasapi.md) per le operazioni di gestione del flusso, ad esempio l'avvio e l'arresto del flusso, il cambio di flusso.
-   [DeviceTopology](devicetopology-api.md) per l'enumerazione di schede audio.
-   [EndpointVolume](endpointvolume-api.md) controllano i livelli di volume delle [sessioni audio](audio-sessions.md).

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione                     |
|----------------------------------------------------------------|-----------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o versioni successive      |
| Visual Studio                                                  | 2005 (edizioni non Express) |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ AECMicArray \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio AecSDKDemo, seguire questa procedura:

1.  Aprire una finestra di comando di SDK.
2.  Digitare **CD% MSSDK% \\ Setup**.
3.  Eseguire VCIntegrate.exe.

    Da questo punto in poi, le finestre di comando avranno le impostazioni di ambiente appropriate per creare un'applicazione che sfrutta i vantaggi dell'SDK.

4.  Compilare l'esempio.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile AecSDKDemo.exe. Per eseguirlo, digitare `AecSDKDemo` una finestra di comando seguita da argomenti obbligatori o facoltativi, come descritto di seguito.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

La tabella seguente illustra gli argomenti.

| Argomento  | Descrizione                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Obbligatorio. Specifica il nome del file di output.                                                                                                 |
| -mod      | Obbligatorio. Specifica la modalità del sistema di acquisizione voce. Per informazioni dettagliate, vedere la sezione "configurazione della funzionalità di acquisizione voce DMO" nel file Leggimi di esempio. |
| -feat     | facoltativo. Attiva la modalità della funzionalità attivata (1) o disattivata (0).                                                                                       |
| -NS       | facoltativo. Attiva l'eliminazione del rumore (1) o disattivato (0). Per specificare questa opzione, è necessario che la modalità funzionalità sia attiva.                                     |
| -AGC      | facoltativo. Attiva il CAG digitale (1) o disattivato (0). Per specificare questa opzione, è necessario che la modalità funzionalità sia attiva.                                           |
| -cntrclip | facoltativo. Attiva il ritaglio al centro (1) o disattivato (0). Per specificare questa opzione, è necessario che la modalità funzionalità sia attiva.                                       |
| -spkdev   | facoltativo. Specifica l'indice del dispositivo speaker. Se non specificato, all'utente verrà richiesto di effettuare la selezione.                                         |
| -micdev   | facoltativo. Specifica l'indice del dispositivo microfonico. Se non specificato, all'utente verrà richiesto di effettuare la selezione.                                      |
| -durata | facoltativo. Specifica la durata dell'esecuzione dell'applicazione.                                                                                    |



 

Questa applicazione di esempio non riproduce alcun segnale. Per eseguire la demo correttamente per le modalità abilitate per AEC (modalità 0 e 4), gli utenti devono riprodurre alcuni segnali audio tramite lo stesso dispositivo speaker specificato per DMO (ovvero il dispositivo specificato dall'opzione "-spkdev"), che simula la voce finale in uno scenario di chat bidirezionale. Gli utenti possono usare qualsiasi lettore per riprodurre segnali audio. Se non è presente alcun flusso di rendering attivo sul dispositivo altoparlante selezionato, l'operazione DMO non verrà elaborata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



