---
description: Viene illustrato come creare un verbo che opera su un elemento o un contenitore della shell selezionato per creare una playlist.
title: Esempio di autore di playlist
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980922"
---
# <a name="playlist-creator-sample"></a>Esempio di autore di playlist

Viene illustrato come creare un verbo che opera su un elemento o un contenitore della shell selezionato per creare una playlist.

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

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio PlaylistCreator](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **PlaylistCreator** .
2.  Immettere `msbuild PlaylistCreator.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

> [!Note]  
> Questo esempio può essere usato anche con il Visual C++ Express Edition se la versione completa di Visual Studio non è disponibile.

 

1.  Aprire Esplora risorse e passare alla directory del progetto **PlaylistCreator** .
2.  Fare doppio clic sull'icona per il file PlaylistCreator. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .
    > [!Note]  
    > Se si compila 64 bit usando il Visual C++ Express Edition, è necessario usare il compilatore incrociato x64 fornito con l'Windows SDK.

     

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `PlaylistCreator.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per PlaylistCreator.exe.
3.  Fare clic con il pulsante destro del mouse su qualsiasi file o cartella musicale contenente file musicali in Esplora risorse per creare una playlist per visualizzare il menu di scelta rapida
4.  È possibile creare una playlist con estensione M3U o WPL. Le playlist vengono create nella `%userprofile%\Music\Playlists` cartella.
    > [!Note]  
    > I nuovi verbi nel menu di scelta rapida sono disponibili nella cartella **Music** , nello stack di musica, negli stack della **raccolta musicale** e nelle raccolte di file musicali.

     

 

 



