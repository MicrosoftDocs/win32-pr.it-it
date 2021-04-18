---
title: Aggiunta di una playlist
description: Aggiunta di una playlist
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- creazione di interfacce, playlist
- Interfacce di Media Player Windows, playlist
- interfacce, playlist
- playlist, interfacce
- playlist di metafile, interfacce
- Playlist Windows Media Metafile, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298575"
---
# <a name="adding-a-playlist"></a>Aggiunta di una playlist

È possibile usare le playlist per scegliere tra raccolte di audio e video.

Usando l'immagine dalla prima interfaccia, è possibile apportare alcune modifiche al file di definizione dell'interfaccia.

Il primo passaggio consiste nell'usare la shell che verrà usata per la maggior parte delle interfacce:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



Aggiungere ora una seconda **visualizzazione** che contiene una playlist. Inserire il codice seguente dopo il </VIEW> del codice della shell.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



È necessario assegnare a questa seconda visualizzazione un ID per potervi fare riferimento in un secondo momento. Aggiungere un oggetto PLAYelement e un oggetto STOPelement. Questi pulsanti predefiniti semplificano la vita.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Infine, aggiungere un evento OnClick all'oggetto PLAYelement per visualizzare una playlist nella seconda visualizzazione:


```C++
            onClick = "JScript: theme.openView('playview');" />

```



Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia della playlist di lavoro simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




