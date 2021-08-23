---
description: Illustra come creare un verbo che opera su un elemento o un contenitore shell selezionato per creare una playlist.
title: Esempio di autore di playlist
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 086cb0f3fbb4cb009cd156013ce3ea16a2a7dee3b2346824d51b79094c06c45e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592891"
---
# <a name="playlist-creator-sample"></a>Esempio di autore di playlist

Illustra come creare un verbo che opera su un elemento o un contenitore shell selezionato per creare una playlist.

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Località      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di PlaylistCreator](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto PlaylistCreator.**
2.  Immettere `msbuild PlaylistCreator.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

> [!Note]  
> Questo esempio può essere usato anche con Visual C++ Express Edition se il Visual Studio completo non è disponibile.

 

1.  Aprire Windows Explorer e passare alla directory del progetto **PlaylistCreator.**
2.  Fare doppio clic sull'icona per il file PlaylistCreator.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.
    > [!Note]  
    > Se si esegue la compilazione a 64 bit con Visual C++ Express Edition, è necessario usare il compilatore incrociato x64 fornito con Windows SDK.

     

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `PlaylistCreator.exe` . In alternativa, da esplora Windows fare doppio clic sull'icona per PlaylistCreator.exe.
3.  Fare clic con il pulsante destro del mouse su qualsiasi file musicale o cartella contenente file musicali in Windows Explorer per creare una playlist per visualizzare il menu di scelta rapida
4.  È possibile creare una playlist con estensione m3u o wpl. Le playlist vengono create nella `%userprofile%\Music\Playlists` cartella .
    > [!Note]  
    > I nuovi verbi nel menu di scelta rapida sono disponibili nella cartella **Musica,** negli stack di musica, negli stack nella libreria **Musica** e nelle raccolte di file musicali.

     

 

 



