---
description: Questa applicazione di esempio usa le API Core Audio per modificare il volume del dispositivo, come specificato dall'utente.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c157149e6b15014b1228b2b5c97080fcdbdccd9acc2745ee5a986a7de7c997f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828272"
---
# <a name="endpointvolume"></a>EndpointVolume

Questa applicazione di esempio usa le API Core Audio per modificare il volume del dispositivo, come specificato dall'utente.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio illustra le funzionalità seguenti.

-   [API MMDevice per](mmdevice-api.md) l'enumerazione e la selezione di dispositivi multimediali.
-   [API EndpointVolume](endpointvolume-api.md) per controllare i livelli di volume dell'endpoint del dispositivo.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località    | Percorso/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi Microsoft SDK Windows \\ \\ \\ v7.0 \\ Samples \\ Multimedia Audio \\ \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio x, seguire questa procedura:

Per compilare l'esempio EndpointVolumeChanger, seguire questa procedura:

1.  Aprire la shell CMD per Windows SDK e passare alla directory di esempio EndpointVolume.
2.  Eseguire il `start EndpointVolumeChanger.sln` comando nella directory EndpointVolume per aprire il progetto EndpointVolumeChanger nella finestra Visual Studio.
3.  Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto WASAPIEndpointVolume.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

Se si compila correttamente l'applicazione demo, viene generato un file eseguibile, EndpointVolumeChanger.exe file. Per eseguirlo, digitare `EndpointVolumeChanger` in una finestra di comando seguita da argomenti obbligatori o facoltativi. L'esempio seguente illustra come attivare o disattivare l'impostazione di disattivazione dell'audio nel dispositivo console predefinito.

`EndpointVolumeChanger.exe -console -m`

Nella tabella seguente vengono illustrati gli argomenti .

| Argomento        | Descrizione                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Visualizza la Guida.                                                         |
| -H              | Visualizza la Guida.                                                         |
| -+              | Incrementa di un passaggio il livello di volume nel dispositivo endpoint audio. . |
| -up             | Incrementa di un passaggio il livello di volume nel dispositivo endpoint audio.   |
| --              | Decrementa di un passaggio il livello di volume nel dispositivo endpoint audio.   |
| -down           | Decrementa di un passaggio il livello di volume nel dispositivo endpoint audio.   |
| -v              | Imposta il livello del volume master nel dispositivo endpoint audio.          |
| -console        | Usare il dispositivo console predefinito.                                     |
| -communications | Usare il dispositivo di comunicazione predefinito.                               |
| -multimedia     | Usare il dispositivo multimediale predefinito.                                  |
| -endpoint       | Usare l'identificatore dell'endpoint specificato nel valore dell'opzione.          |



 

Se l'applicazione viene eseguita senza argomenti, enumera i dispositivi disponibili e richiede all'utente di selezionare un dispositivo. Dopo che l'utente ha specificato il dispositivo, l'applicazione visualizza le impostazioni correnti del volume per l'endpoint. Il volume può essere controllato usando le opzioni descritte nella tabella precedente.

Per altre informazioni sul controllo dei livelli di volume dei dispositivi endpoint audio, vedere [Api EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



