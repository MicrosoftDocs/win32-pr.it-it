---
description: Questa applicazione di esempio usa le API audio principali per modificare il volume del dispositivo, come specificato dall'utente.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483492"
---
# <a name="endpointvolume"></a>EndpointVolume

Questa applicazione di esempio usa le API audio principali per modificare il volume del dispositivo, come specificato dall'utente.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   [API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.
-   [API EndpointVolume](endpointvolume-api.md) per controllare i livelli di volume dell'endpoint del dispositivo.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio x, attenersi alla procedura seguente:

Per compilare l'esempio EndpointVolumeChanger, seguire questa procedura:

1.  Aprire la shell CMD per la Windows SDK e passare alla directory di esempio EndpointVolume.
2.  Eseguire il comando `start EndpointVolumeChanger.sln` nella directory EndpointVolume per aprire il progetto EndpointVolumeChanger nella finestra di Visual Studio.
3.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto, WASAPIEndpointVolume. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se l'applicazione demo viene compilata correttamente, viene generato un file eseguibile EndpointVolumeChanger.exe. Per eseguirlo, digitare `EndpointVolumeChanger` in una finestra di comando seguita da argomenti obbligatori o facoltativi. Nell'esempio seguente viene illustrato come attivare o disattivare l'impostazione di silenziamento sul dispositivo predefinito della console.

`EndpointVolumeChanger.exe -console -m`

La tabella seguente illustra gli argomenti.

| Argomento        | Descrizione                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Visualizza la guida.                                                         |
| -H              | Visualizza la guida.                                                         |
| -+              | Incrementa il livello del volume sul dispositivo dell'endpoint audio di un solo passaggio. . |
| -su             | Incrementa il livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.   |
| --              | Decrementa del livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.   |
| -giù           | Decrementa del livello del volume sul dispositivo dell'endpoint audio di un solo passaggio.   |
| -v              | Imposta il livello del volume master sul dispositivo dell'endpoint audio.          |
| -Console        | Usare il dispositivo console predefinito.                                     |
| -comunicazioni | Usare il dispositivo di comunicazione predefinito.                               |
| -Multimedia     | Usare il dispositivo multimediale predefinito.                                  |
| -endpoint       | Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.          |



 

Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e chiede all'utente di selezionare un dispositivo. Dopo che l'utente ha specificato il dispositivo, l'applicazione Visualizza le impostazioni correnti del volume per l'endpoint. Il volume può essere controllato usando le opzioni descritte nella tabella precedente.

Per altre informazioni sul controllo dei livelli di volume dei dispositivi dell'endpoint audio, vedere [API EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



