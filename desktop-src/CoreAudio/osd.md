---
description: Questo esempio usa le API audio principali per implementare una visualizzazione sullo schermo che mostra le modifiche del volume al flusso di output che riproduce il dispositivo dell'endpoint di rendering audio predefinito.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049216"
---
# <a name="osd"></a>OSD

Questo esempio usa le API audio principali per implementare una visualizzazione sullo schermo che mostra le modifiche del volume al flusso di output che riproduce il dispositivo dell'endpoint di rendering audio predefinito. La visualizzazione sullo schermo viene visualizzata quando l'utente regola il livello del volume nel programma di controllo del volume di Windows, Sndvol.exe e scompare dopo che il livello del volume rimane invariato per un breve periodo di tempo.

Questo argomento contiene le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

In questo esempio vengono illustrate le funzionalità seguenti.

-   [API MMDevice](mmdevice-api.md) per la selezione e l'enumerazione dei dispositivi multimediali.
-   [API EndpointVolume](endpointvolume-api.md) audio

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o versioni successive |
| Visual Studio                                                  | 2005 o versione successiva          |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Location    | Percorso/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v 7.0 esempi di \\ \\ audio multimediale \\ \\ OSD \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

1.  Aprire la shell CMD per la Windows SDK e passare alla directory di esempio OSD.
2.  Eseguire il comando "Start OSD. sln" nella directory OSD per aprire il progetto OSD nella finestra di Visual Studio.
3.  Nella finestra di selezionare la configurazione di **debug** o di **rilascio** della soluzione, selezionare il menu **Compila** dalla barra dei menu e selezionare l'opzione **Compila** . Se non si apre Visual Studio dalla shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione dell'SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposti in modo esplicito la variabile di ambiente MSSdk, che viene usata nel file di progetto OSD. vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Eseguire il file eseguibile OSD, OSD.exe, in Windows Vista o versioni successive. Si noti che non viene visualizzata un'icona della barra delle applicazioni o una finestra per l'applicazione, ma è possibile vedere il processo in esecuzione utilizzando TaskMgr.exe.
2.  Eseguire sndvol.exe per modificare il volume o il mute oppure modificare il volume utilizzando i controlli della tastiera o un controllo nascosto. Verrà visualizzata l'interfaccia utente OSD.
3.  Per uscire dall'applicazione, eseguire TaskMgr.exe, evidenziare il processo di OSD.exe e fare clic su **Termina processo**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio principali](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



