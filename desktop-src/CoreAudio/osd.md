---
description: Questo esempio usa le API Core Audio per implementare uno schermo su schermo che mostra le modifiche del volume al flusso di output riprodotto tramite il dispositivo endpoint di rendering audio predefinito.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Osd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bc0b93214cc547f0491d568abb88d696f76b494f2c562f4805f425acdcfd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077515"
---
# <a name="osd"></a>Osd

Questo esempio usa le API Core Audio per implementare uno schermo su schermo che mostra le modifiche del volume al flusso di output riprodotto tramite il dispositivo endpoint di rendering audio predefinito. La visualizzazione su schermo viene visualizzata quando l'utente regola il livello del volume nel programma di controllo del volume Windows, Sndvol.exe, e scompare dopo che il livello del volume rimane invariato per un breve periodo.

Questo argomento contiene le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="description"></a>Descrizione

Questo esempio illustra le funzionalità seguenti.

-   [API MMDevice per](mmdevice-api.md) l'enumerazione e la selezione di dispositivi multimediali.
-   API [Audio EndpointVolume](endpointvolume-api.md)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o versioni successive |
| Visual Studio                                                  | 2005 o versione successiva          |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nelle posizioni seguenti.



| Località    | Percorso/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Programmi \\ Microsoft SDK \\ Windows \\ v7.0 \\ \\ Samples Multimedia Audio \\ \\ OSD \\ ... |



 

## <a name="building-the-sample"></a>Compilazione dell'esempio

1.  Aprire la shell CMD per Windows SDK e passare alla directory di esempio OSD.
2.  Eseguire il comando "start OSD.sln" nella directory OSD per aprire il progetto OSD nella Visual Studio finestra.
3.  Nella finestra selezionare la configurazione  della soluzione **Debug** o Versione, scegliere il **menu** Compila dalla barra dei menu e selezionare l'opzione **Compila.** Se non si apre Visual Studio shell CMD per l'SDK, Visual Studio non avrà accesso all'ambiente di compilazione SDK. In tal caso, l'esempio non verrà compilato a meno che non si imposta in modo esplicito la variabile di ambiente MSSdk, usata nel file di progetto OSD.vcproj.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Eseguire il file eseguibile OSD, OSD.exe, in Windows Vista o versione successiva. Si noti che non verrà visualizzata un'icona della barra delle applicazioni o una finestra per l'applicazione, ma è possibile visualizzare il processo in esecuzione usando TaskMgr.exe.
2.  Eseguire sndvol.exe per modificare il volume o disattivare l'audio o modificare il volume usando i controlli della tastiera o un controllo HID. Viene visualizzata l'interfaccia utente OSD.
3.  Per uscire dall'applicazione, eseguire TaskMgr.exe, evidenziare OSD.exe processo e fare clic **su Termina processo**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di SDK che usano le API audio di base](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



